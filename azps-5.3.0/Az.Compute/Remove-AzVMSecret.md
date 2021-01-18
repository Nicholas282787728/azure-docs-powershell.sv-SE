---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526739"
---
# <span data-ttu-id="57623-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="57623-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="57623-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57623-102">SYNOPSIS</span></span>
<span data-ttu-id="57623-103">Tar bort (a) hemliga (a) hemligheter från ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="57623-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="57623-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57623-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57623-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57623-105">DESCRIPTION</span></span>
<span data-ttu-id="57623-106">Remove-AzVMSecret-cmdleten tar bort (a) hemligheter från ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="57623-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="57623-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57623-107">EXAMPLES</span></span>

### <span data-ttu-id="57623-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="57623-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="57623-109">Tar bort alla hemligheter från en virtuell dator "VM1" i resurs gruppen "RG1" och uppdaterar den virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="57623-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="57623-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57623-110">PARAMETERS</span></span>

### <span data-ttu-id="57623-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57623-111">-DefaultProfile</span></span>
<span data-ttu-id="57623-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57623-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57623-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="57623-113">-SourceVaultId</span></span>
<span data-ttu-id="57623-114">Anger en matris med käll valv-ID: n som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="57623-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57623-115">-VM</span><span class="sxs-lookup"><span data-stu-id="57623-115">-VM</span></span>
<span data-ttu-id="57623-116">Anger den virtuella dator från vilken denna cmdlet tar bort (a) hemlighet (s).</span><span class="sxs-lookup"><span data-stu-id="57623-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="57623-117">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="57623-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="57623-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57623-118">-Confirm</span></span>
<span data-ttu-id="57623-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57623-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57623-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57623-120">-WhatIf</span></span>
<span data-ttu-id="57623-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57623-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57623-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57623-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57623-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57623-123">CommonParameters</span></span>
<span data-ttu-id="57623-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57623-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57623-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57623-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57623-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57623-126">INPUTS</span></span>

### <span data-ttu-id="57623-127">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="57623-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="57623-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57623-128">OUTPUTS</span></span>

### <span data-ttu-id="57623-129">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="57623-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="57623-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57623-130">NOTES</span></span>

## <span data-ttu-id="57623-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57623-131">RELATED LINKS</span></span>
