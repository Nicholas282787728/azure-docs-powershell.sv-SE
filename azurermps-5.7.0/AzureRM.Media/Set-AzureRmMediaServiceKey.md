---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 2b0e8564f2a536c7b7eda5b9ae8ae3cc58bf41cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755867"
---
# Set-AzureRmMediaServiceKey

## Sammanfattning
Återskapar en nyckeln som används för att komma åt den REST-slutpunkt som är associerad med medie tjänsten.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmMediaServiceKey** återskapar en nyckeln som används för att öppna den ompresentations tillstånds överföring (rest) som är associerad med medie tjänsten.

## BESKRIVS

### Exempel 1: återskapa den primära nyckeln som används för åtkomst till medie tjänsten
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

Det här kommandot återskapar primär nyckeln för medie tjänsten som heter MediaService001 som tillhör resurs gruppen med namnet ResourceGroup004.

### Exempel 2: återskapa den sekundära nyckeln som används för åtkomst till medie tjänsten
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

Det här kommandot återskapar den sekundära nyckeln för medie tjänsten som heter MediaService002 som tillhör resurs gruppen med namnet Resourcegroup123.

## MALLPARAMETRAR

### -AccountName
Anger namnet på den medie tjänst som denna cmdlet ska återskapa.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Värdetyp
Anger medie tjänstens medietyp.
De acceptabla värdena för den här parametern är: primär eller sekundär.

```yaml
Type: KeyType
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som innehåller medie tjänsten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. Media. Models. PSServiceKey

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmMediaServiceKeys](./Get-AzureRmMediaServiceKeys.md)


