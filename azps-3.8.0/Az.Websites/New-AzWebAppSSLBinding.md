---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1f43b551a24cc0e98c3c42322b030549a74938
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088460"
---
# New-AzWebAppSSLBinding

## Sammanfattning
Skapar en SSL-certifikatfil för en Azure Web App.

## FRÅGESYNTAXEN

### S
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzWebAppSSLBinding** skapar ett SSL-certifikat (Secure Socket Layer) för en Azure Web App.
Cmdleten skapar en SSL-bindning på två sätt: 
- Du kan binda ett webb program till ett befintligt certifikat.
- Du kan ladda upp ett nytt certifikat och sedan binda det till det nya certifikatet.
Oavsett vilken metod du använder måste certifikatet och webb programmet vara associerat med samma Azure Resource Group.
Om du har ett webb program i resurs grupp A och du vill binda det webb programmet till ett certifikat i resurs grupp B är det enda sättet att göra det till att ladda upp en kopia av certifikatet till resurs gruppen A. Om du laddar upp ett nytt certifikat bör du tänka på följande krav för ett Azure SSL-certifikat: 
- Certifikatet måste innehålla en privat. 
- Certifikatet måste ha formatet PFX (personal information Exchange). 
- Certifikatets subjekt namn måste stämma överens med den domän som används för att komma åt webb programmet. 
- Certifikatet måste innehålla minst 2048-bitars kryptering.

## BESKRIVS

### Exempel 1: binda ett certifikat till ett webb program
```
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Det här kommandot binder ett befintligt Azure-certifikat (ett certifikat med tumavtrycket E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) till webb programmet som heter ContosoWebApp.

## MALLPARAMETRAR

### -CertificateFilePath
Anger sökvägen för det certifikat som ska laddas upp.
Parametern *CertificateFilePath* krävs bara om certifikatet inte ännu har laddats upp till Azure.

```yaml
Type: System.String
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
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på webb programmet.

```yaml
Type: System.String
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
Type: System.String
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
Du kan använda Get-AzWebAppSlot cmdlet för att få en kort plats.
Distributions platser är ett sätt för dig att mellanlagra och validera webb program utan att programmen är tillgängliga via Internet.
Vanligt vis distribuerar du dina ändringar på en mellanlagringsdatabas, validerar dessa ändringar och sedan distribuerar till produktions webbplatsen (Internet-tillgänglig).

```yaml
Type: System.String
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
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
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
Type: System.String
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
Om du vill hämta en webbapp använder du Get-AzWebApp cmdlet.
Du kan inte använda *webapp* -parametern i samma kommando som parametern *ResourceGroupName* och/eller *WebAppName*.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
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
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. webapps. Models. PSSite

## VÄRDEN

### Microsoft. Azure. Management. webbplatser. Models. HostNameSslState

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


