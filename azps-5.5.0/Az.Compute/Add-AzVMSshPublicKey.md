---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233422"
---
# Add-AzVMSshPublicKey

## SYNOPSIS
Lägger till offentliga nycklar för SSH för en virtuell dator när du bara skapar den virtuella datorn.

## SYNTAX

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzVMSshPublicKey** lägger till de offentliga nycklar som du kan använda för att ansluta till en virtuell Linux-dator via Secure Shell (SSH). Det här kan inte användas efter att VM har skapats. Om du försöker använda det här när vm har skapats utan Uppdatering-AzVM blir det inget fel. Om du använder kommandot med Update-AzVM kommer kommandot att visas som ett fel.

## EXEMPEL

### Exempel 1: Lägga till en offentlig nyckel till en virtuell dator
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

Det första kommandot hämtar den virtuella datorn med namnet VirtualMa machinee07 med hjälp av **Get-AzVM-cmdleten.**
Kommandot lagrar den virtuella datorn i $VirtualMachine variabeln.
Det andra kommandot lägger till den offentliga nyckeln på platsen på VirtualMachine07 som sökvägsparametern anger.

## PARAMETERS

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

### -KeyData
Anger en bas 64-kodning av en offentlig nyckel.
Du kan ansluta till en virtuell Linux-dator med hjälp av SSH eller genom att använda nyckeln som den här parametern anger.

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

### -Path
Anger den fullständiga sökvägen till en fil på den virtuella datorn där den här cmdleten lagrar den offentliga SSH-nyckeln.
Om filen redan finns lägger denna cmdlet till nyckeln i filen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Anger det virtuella datorobjektet som denna cmdlet ändrar.
Om du vill hämta ett virtuellt datorobjekt använder [du cmdleten Get-AzVM.](./Get-AzVM.md)
Du kan använda cmdleten [New-AzVMConfig](./New-AzVMConfig.md) till att skapa ett virtuellt datorobjekt.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## UTDATA

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
