---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fc8e454328706243e701c0f4df61733562ab73ce
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924062"
---
# Get-AzADAppCredential

## Sammanfattning
Hämtar en lista med autentiseringsuppgifter som är associerade med ett program.

## FRÅGESYNTAXEN

### ApplicationObjectIdParameterSet (standard)
```
Get-AzADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Med cmdleten Get-AzADAppCredential kan du hämta en lista med autentiseringsuppgifter som är associerade med ett program.
Det här kommandot hämtar alla autentiseringsuppgifter-egenskaper (men inte referensvärdet) som är associerade med programmet.

## BESKRIVS

### Exempel 1 – få programautentisering genom objekt-ID

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

Returnerar en lista med autentiseringsuppgifter som är kopplade till programmet med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.

### Exempel 2 – få programautentiseringsuppgifter genom rör

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

Hämtar programmet med objekt-ID ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' och kopplas till Get-AzADAppCredential cmdlet för att lista alla autentiseringsuppgifter för det programmet.

## MALLPARAMETRAR

### -ApplicationId
ID för programmet som autentiseringsuppgifterna hämtas från.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
Application-objektet som autentiseringsuppgifterna hämtas från.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Programmets visnings namn.

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Objekt-ID för programmet som du vill hämta autentiseringsuppgifter från.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. GUID

### System. String

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication
Parametrar: ApplicationObject (ByValue)

## VÄRDEN

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzADAppCredential](./New-AzADAppCredential.md)

[Remove-AzADAppCredential](./Remove-AzADAppCredential.md)

[Get-AzADApplication](./Get-AzADApplication.md)

