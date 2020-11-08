---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091395"
---
# <span data-ttu-id="854a9-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="854a9-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="854a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="854a9-102">SYNOPSIS</span></span>
<span data-ttu-id="854a9-103">Tar bort (a) hemliga (a) hemligheter från ett virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="854a9-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="854a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="854a9-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="854a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="854a9-105">DESCRIPTION</span></span>
<span data-ttu-id="854a9-106">Remove-AzVMSecret-cmdleten tar bort (a) hemligheter från ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="854a9-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="854a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="854a9-107">EXAMPLES</span></span>

### <span data-ttu-id="854a9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="854a9-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="854a9-109">Tar bort alla hemligheter från en virtuell dator "VM1" i resurs gruppen "RG1" och uppdaterar den virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="854a9-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="854a9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="854a9-110">PARAMETERS</span></span>

### <span data-ttu-id="854a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="854a9-111">-DefaultProfile</span></span>
<span data-ttu-id="854a9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="854a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="854a9-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="854a9-113">-SourceVaultId</span></span>
<span data-ttu-id="854a9-114">Anger en matris med käll valv-ID: n som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="854a9-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="854a9-115">-VM</span><span class="sxs-lookup"><span data-stu-id="854a9-115">-VM</span></span>
<span data-ttu-id="854a9-116">Anger den virtuella dator från vilken denna cmdlet tar bort (a) hemlighet (s).</span><span class="sxs-lookup"><span data-stu-id="854a9-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="854a9-117">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="854a9-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="854a9-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="854a9-118">-Confirm</span></span>
<span data-ttu-id="854a9-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="854a9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="854a9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="854a9-120">-WhatIf</span></span>
<span data-ttu-id="854a9-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="854a9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="854a9-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="854a9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="854a9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854a9-123">CommonParameters</span></span>
<span data-ttu-id="854a9-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="854a9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854a9-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="854a9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854a9-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="854a9-126">INPUTS</span></span>

### <span data-ttu-id="854a9-127">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="854a9-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="854a9-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="854a9-128">OUTPUTS</span></span>

### <span data-ttu-id="854a9-129">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="854a9-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="854a9-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="854a9-130">NOTES</span></span>

## <span data-ttu-id="854a9-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="854a9-131">RELATED LINKS</span></span>
