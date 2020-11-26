---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 2c36408b520268acaaa6ae2fa4c4c6030fbd2111
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324755"
---
# <span data-ttu-id="0b142-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0b142-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="0b142-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b142-102">SYNOPSIS</span></span>
<span data-ttu-id="0b142-103">Hämtar egenskaper för virtuella dator tillägg som är installerade på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0b142-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="0b142-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b142-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b142-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b142-105">DESCRIPTION</span></span>
<span data-ttu-id="0b142-106">Cmdleten **Get-AzVMExtension** hämtar egenskaper för virtuella dator tillägg som är installerade på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0b142-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="0b142-107">Ange namnet på ett tillägg som du vill hämta egenskaper för.</span><span class="sxs-lookup"><span data-stu-id="0b142-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="0b142-108">Om du bara vill få instans visningen av ett fil namn anger du en status parameter.</span><span class="sxs-lookup"><span data-stu-id="0b142-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="0b142-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b142-109">EXAMPLES</span></span>

### <span data-ttu-id="0b142-110">Exempel 1: Hämta egenskaper för ett tillägg</span><span class="sxs-lookup"><span data-stu-id="0b142-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="0b142-111">Det här kommandot får egenskaper för tillägget som heter CustomScriptExtension på den virtuella datorn med namnet VirtualMachine22 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0b142-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="0b142-112">Exempel 2: Hämta instans visning av ett tillägg</span><span class="sxs-lookup"><span data-stu-id="0b142-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="0b142-113">Med det här kommandot hämtas instans-vyn för tillägget som heter CustomScriptExtension på den virtuella datorn med namnet VirtualMachine22 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0b142-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="0b142-114">Exempel 3: Hämta alla tillägg på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="0b142-114">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="0b142-115">Det här kommandot får listan över tillägg som är installerade på den virtuella datorn med namnet VirtualMachine22 i ResourceGroup11 för resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0b142-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="0b142-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b142-116">PARAMETERS</span></span>

### <span data-ttu-id="0b142-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b142-117">-DefaultProfile</span></span>
<span data-ttu-id="0b142-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b142-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b142-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0b142-119">-Name</span></span>
<span data-ttu-id="0b142-120">Anger namnet på ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="0b142-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="0b142-121">Denna cmdlet hämtar egenskaper för tillägget som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0b142-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b142-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b142-122">-ResourceGroupName</span></span>
<span data-ttu-id="0b142-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0b142-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b142-124">-Status</span><span class="sxs-lookup"><span data-stu-id="0b142-124">-Status</span></span>
<span data-ttu-id="0b142-125">Anger att denna cmdlet bara får instans vyn av ett tillägg.</span><span class="sxs-lookup"><span data-stu-id="0b142-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b142-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="0b142-126">-VMName</span></span>
<span data-ttu-id="0b142-127">Anger namnet på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0b142-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0b142-128">Denna cmdlet hämtar egenskaper för ett tillägg från den virtuella dator som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0b142-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b142-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b142-129">CommonParameters</span></span>
<span data-ttu-id="0b142-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b142-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b142-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b142-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b142-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b142-132">INPUTS</span></span>

### <span data-ttu-id="0b142-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0b142-133">System.String</span></span>

### <span data-ttu-id="0b142-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0b142-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0b142-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b142-135">OUTPUTS</span></span>

### <span data-ttu-id="0b142-136">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="0b142-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="0b142-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b142-137">NOTES</span></span>

## <span data-ttu-id="0b142-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b142-138">RELATED LINKS</span></span>

[<span data-ttu-id="0b142-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0b142-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="0b142-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="0b142-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

