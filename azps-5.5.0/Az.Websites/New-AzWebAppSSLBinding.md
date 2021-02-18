---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100253409"
---
# New-AzWebAppSSLBinding

## SYNOPSIS
Skapar en SSL-certifikatbindning för en Azure Web App.

## SYNTAX

### S1
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

## BESKRIVNING
Den **nya cmdleten AzWebAppSSLBinding** skapar en SSL-certifikatbindning (Secure Socket Layer) för en Azure Web App.
Cmdleten skapar en SSL-bindning på två sätt: 
- Du kan binda en webbapp till ett befintligt certifikat.
- Du kan ladda upp ett nytt certifikat och sedan binda Webbappen till det här nya certifikatet.
Oavsett vilken metod du använder måste certifikatet och webbappen vara associerade med samma Azure-resursgrupp.
Om du har ett webbapp i resursgrupp A och du vill binda det webbprogrammet till ett certifikat i resursgrupp B kan du bara ladda upp en kopia av certifikatet till Resursgrupp A. Om du laddar upp ett nytt certifikat bör du tänka på följande krav för ett Azure SSL-certifikat: 
- Certifikatet måste innehålla en privat nyckel. 
- Certifikatet måste använda formatet PFX (Personal Information Exchange). 
- Certifikatets ämnesnamn måste matcha den domän som används för att komma åt Web App. 
- Certifikatet måste använda minst 2048-bitars kryptering.

## EXEMPEL

### Exempel 1: Binda ett certifikat till en webbapp
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

Det här kommandot binder ett befintligt Azure-certifikat (ett certifikat med Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) till webbappen ContosoWebApp.

### Exempel 2

Skapar en SSL-certifikatbindning för en Azure Web App. (autogenererat)

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## PARAMETERS

### -CertificateFilePath
Anger filsökvägen för det certifikat som ska laddas upp.
Parametern *CertificateFilePath* krävs bara om certifikatet ännu inte har laddats upp till Azure.

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
Anger dekrypteringslösenordet för certifikatet.

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -Name
Anger namnet på webbappen.

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
Anger namnet på den resursgrupp som certifikatet är tilldelat till.
Du kan inte använda *parametern ResourceGroupName* och *WebApp* i samma kommando.

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

### -Slot
Anger namnet på Web App-distributionsplats.
Du kan använda cmdlet Get-AzWebAppSlot för att få en kortplats.
Distributionsplatser är ett sätt för dig att fasa in och validera webbappar utan att apparna är tillgängliga via Internet.
Vanligtvis distribuerar du ändringarna till en mellanlagringswebbplats, verifierar ändringarna och distribuerar sedan till produktionswebbplatsen (Internettillgänglig).

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
Ställ in *SSLState-parametern* på 1 för att aktivera certifikatet eller ange *SSLState* till 0 för att inaktivera certifikatet.

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

### -Thumbprint
Anger unik identifierare för certifikatet.

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
Anger en webbapp.
Om du vill skaffa en webbapp använder du Get-AzWebApp-cmdleten.
Du kan inte använda *WebApp-parametern* i samma kommando som *ResourceGroupName-parametern* och/eller *WebAppName.*

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
Anger namnet på webbappen som den nya SSL-bindningen skapas för.
Du kan inte använda *WebAppName-parametern* *och WebApp-parametern* i samma kommando.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## UTDATA

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzWebAppsSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppsSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


