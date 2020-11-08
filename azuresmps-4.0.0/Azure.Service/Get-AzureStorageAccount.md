---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093275"
---
# Get-AzureStorageAccount

## Sammanfattning
Hämtar lagrings konton för det aktuella Azure-abonnemanget.

## FRÅGESYNTAXEN

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorageAccount** returnerar ett objekt som innehåller information om lagrings kontona för det aktuella abonnemanget.
Om parametern *StorageAccountName* anges returneras bara information om det angivna lagrings kontot.

## BESKRIVS

### Exempel 1: returnera alla lagrings konton
```
PS C:\> Get-AzureStorageAccount
```

Det här kommandot returnerar ett objekt med alla lagrings konton som är kopplade till det aktuella abonnemanget.

### Exempel 2: returnera konto information för ett angivet konto
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

Det här kommandot returnerar ett objekt med endast ContosoStore01-konto information.

### Exempel 3: Visa en tabell med lagrings konton
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

Det här kommandot returnerar ett objekt med alla lagrings konton som är kopplade till det aktuella abonnemanget och visar dem som en tabell med konto namnet, konto etiketten och lagrings platsen.

## MALLPARAMETRAR

### -InformationAction
Anger hur den här cmdleten svarar på en informations händelse.

De acceptabla värdena för den här parametern är:

- Vidare
- Över
- Inquire
- SilentlyContinue
- Stanna
- Avbryt

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Anger en informations variabel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Anger namnet på ett lagrings konto.
Om det här alternativet anges returnerar den här cmdleten bara det angivna lagrings konto objekt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### ManagementOperationContext

## ANMÄRKNINGAR
* Skriv `help node-dev` för att få hjälp med Node.js utvecklingsbaserade cmdletar. Skriv `help php-dev` för att få hjälp med relevanta cmdlets för php-utveckling.

## RELATERADE LÄNKAR

[New-AzureStorageAccount](./New-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


