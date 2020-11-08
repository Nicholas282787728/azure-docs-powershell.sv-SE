---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270957"
---
# Get-AzManagedHsm

## Sammanfattning
Skaffa hanterade HSMs.

## FRÅGESYNTAXEN

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzManagedHsm** hämtar information om de hanterade HSMs i ett abonnemang. Du kan visa alla hanterade HSMs-instanser i en prenumeration, eller filtrera dina resultat efter en resurs grupp eller en viss hanterad HSM.
Observera att även om du anger resurs gruppen som valfri för denna cmdlet när du får en enda hanterad HSM bör du göra det för bättre prestanda.

## BESKRIVS

### Exempel 1: Hämta alla hanterade HSMs i ditt nuvarande abonnemang
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Det här kommandot får alla hanterade HSMs i ditt nuvarande abonnemang.

### Exempel 2: Hämta en specifik hanterad HSM
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Det här kommandot får den hanterade HSM som heter myhsm i ditt nuvarande abonnemang.

### Exempel 3: Hämta hanterade HSMs i en resurs grupp
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Det här kommandot får alla hanterade HSMs i resurs gruppen "myrg1".

### Exempel 4: Hämta hanterade HSMs med hjälp av filtrering
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Det här kommandot får alla hanterade HSMs i prenumerationen som börjar med "myhsm".

## MALLPARAMETRAR

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
HSM-namn. Cmdlet konstruerar FQDN för en HSM baserat på namnet och den valda miljön.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resurs grupp som är kopplad till den hanterade HSM som efter frågas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
Anger tangenten och det valfria värdet för den angivna taggen för att filtrera listan med hanterade HSMs.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### System. Collections. hash

## VÄRDEN

### Microsoft. Azure. commands. valv. Models. PSManagedHsm

### Microsoft. Azure. commands. valv. Models. PSKeyVaultIdentityItem

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[New-AzManagedHsm](./New-AzManagedHsm.md)

[Remove-AzManagedHsm](./Remove-AzManagedHsm.md)

[Update-AzManagedHsm](./Update-AzManagedHsm.md)