---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: d3971c2838b3fed04e1aa38d96e2cd27b2e8276e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581867"
---
# New-AzureRmWebAppSSLBinding

## Sammanfattning
Skapar en SSL-certifikatfil för en Azure Web App.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### S
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmWebAppSSLBinding** skapar ett SSL-certifikat (Secure Socket Layer) för en Azure Web App.
Cmdleten skapar en SSL-bindning på två sätt: 

- Du kan binda ett webb program till ett befintligt certifikat.
- Du kan ladda upp ett nytt certifikat och sedan binda det till det nya certifikatet.

Oavsett vilken metod du använder måste certifikatet och webb programmet vara associerat med samma Azure Resource Group.
Om du har ett webb program i resurs grupp A och du vill binda det webb programmet till ett certifikat i resurs grupp B är det enda sättet att göra det till att ladda upp en kopia av certifikatet till resurs gruppen A.

Om du laddar upp ett nytt certifikat bör du tänka på följande krav för ett Azure SSL-certifikat: 

- Certifikatet måste innehålla en privat. 
- Certifikatet måste ha formatet PFX (personal information Exchange). 
- Certifikatets subjekt namn måste stämma överens med den domän som används för att komma åt webb programmet. 
- Certifikatet måste innehålla minst 2048-bitars kryptering.

## BESKRIVS

### Exempel 1: binda ett certifikat till ett webb program
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Det här kommandot binder ett befintligt Azure-certifikat (ett certifikat med tumavtrycket E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) till webb programmet som heter ContosoWebApp.

## MALLPARAMETRAR

### -CertificateFilePath
Anger sökvägen för det certifikat som ska laddas upp.

Parametern *CertificateFilePath* krävs bara om certifikatet inte ännu har laddats upp till Azure.

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Anger krypterings lösen ordet för certifikatet.

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på webb programmet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen som certifikatet har tilldelats till.

Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger namnet på webb programmets distributions plats.
Du kan använda Get-AzureRMWebAppSlot cmdlet för att få en kort plats.

Distributions platser är ett sätt för dig att mellanlagra och validera webb program utan att programmen är tillgängliga via Internet.
Vanligt vis distribuerar du dina ändringar på en mellanlagringsdatabas, validerar dessa ändringar och sedan distribuerar till produktions webbplatsen (Internet-tillgänglig).

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
Anger om certifikatet är aktiverat.
Ställ in parametern *SSLState* på 1 för att aktivera certifikatet, eller ange värdet 0 för *SSLState* om du vill inaktivera certifikatet.

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tumavtryck
Anger det unika ID: t för certifikatet.

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Anger ett webb program.
Om du vill hämta en webbapp använder du Get-AzureRmWebApp cmdlet.

Du kan inte använda *webapp* -parametern i samma kommando som parametern *ResourceGroupName* och/eller *WebAppName*.

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Anger namnet på den webbapp som den nya SSL-bindningen skapas för.

Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Webbplatsmallar
Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[Remove-AzureRmWebAppSSLBinding](./Remove-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


