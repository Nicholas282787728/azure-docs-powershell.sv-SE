---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573776"
---
# Get-AzureRmApiManagementUser

## Sammanfattning
Hämtar en användare eller användare.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### Hämta alla användare (standard)
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Skaffa användare utifrån ID
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Hitta användare
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmApiManagementUser** hämtar en angiven användare eller alla användare om ingen användare har angetts.

## BESKRIVS

### Exempel 1: Hämta alla användare
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

Det här kommandot får alla användare.

### Exempel 2: skaffa en användare utifrån ID
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

Det här kommandot får en användare via ID.

### Exempel: Hämta användare efter efter namn
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

Med det här kommandot får du användare med ett angivet efter namn, fullständig Nilsson.

### Exempel 4: Hämta en användare via e-postadress
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

Det här kommandot får användaren som har angiven e-postadress.

### Exempel 5: samla alla användare i en grupp
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

Det här kommandot får alla användare i den angivna gruppen.

## MALLPARAMETRAR

### -Kontext
Anger en instans av **PsApiManagementContext**.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -E-postadress
Anger användarens e-postadress.
Om den här parametern anges hittas en användare via e-post.
Denna parameter är valfri.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirstName
Anger användarens förnamn.
Om denna parameter anges hittar denna cmdlet en användare via förnamnet.
Denna parameter är valfri.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kund-
Anger grupp-ID.
Om den anges hittar denna cmdlet alla användare i den angivna gruppen.
Denna parameter är valfri.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LastName
Anger användarens efter namn.
Om den här cmdleten anges hittas användare med efter namn.
Denna parameter är valfri.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Anger användar tillståndet.
Om det här alternativet anges hittar denna cmdlet användare i det här tillståndet.
Denna parameter är valfri.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserId
Anger ett användar-ID.
Om det här alternativet anges hittar denna cmdlet användaren med den här identifieraren.
Denna parameter är valfri.

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementUser>

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzureRmApiManagementUser](./New-AzureRmApiManagementUser.md)

[Remove-AzureRmApiManagementUser](./Remove-AzureRmApiManagementUser.md)

[Set-AzureRmApiManagementUser](./Set-AzureRmApiManagementUser.md)


