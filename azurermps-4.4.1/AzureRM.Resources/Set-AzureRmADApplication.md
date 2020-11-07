---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: 6fbbed83f9565a81b305df5cf8b66fd8210c6aec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758009"
---
# Set-AzureRmADApplication

## Sammanfattning
Uppdaterar ett befintligt Azure Active Directory-program.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ApplicationObjectIdWithUpdateParamsParameterSet
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationIdWithUpdateParamsParameterSet
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Uppdaterar ett befintligt Azure Active Directory-program.
Använd New-AzureRmADAppCredential cmdlet för att uppdatera autentiseringsuppgifterna för det här programmet.

## BESKRIVS

### --------------------------Exempel 1--------------------------
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

Uppdaterar egenskaperna för ett befintligt Azure Active Directory-program med objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".

### --------------------------Exempel 2--------------------------
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

Uppdaterar visnings namnet för ett befintligt Azure Active Directory-program med objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".

## MALLPARAMETRAR

### -ApplicationId
ID för programmet som ska uppdateras.

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AvailableToOtherTenants
Det värde som anger om programmet uppdateras till en enskild klient organisation eller en klient organisation.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayName
Nytt visnings namn för programmet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Start Sidan
Ny URL för programmets start sida.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentifierUris
Nya URI: er som identifierar programmet.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Objekt-ID för programmet som ska uppdateras.

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplyUrls
Nya svars-URL: er för programmet.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmADApplication](./Get-AzureRmADApplication.md)

[New-AzureRmADApplication](./New-AzureRmADApplication.md)

[Remove-AzureRmADApplication](./Remove-AzureRmADApplication.md)

[New-AzureRmADAppCredential](./New-AzureRmADAppCredential.md)

[Get-AzureRmADAppCredential](./Get-AzureRmADAppCredential.md)

[Remove-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)

