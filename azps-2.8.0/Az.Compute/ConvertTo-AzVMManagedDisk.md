---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 71cbd99ccd34341eb996cd4015f9e8c39d9c7fa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745221"
---
# <span data-ttu-id="f980f-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="f980f-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="f980f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f980f-102">SYNOPSIS</span></span>
<span data-ttu-id="f980f-103">Konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="f980f-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="f980f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f980f-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f980f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f980f-105">DESCRIPTION</span></span>
<span data-ttu-id="f980f-106">**ConvertTo-AzVMManagedDisk-** cmdlet konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="f980f-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="f980f-107">Den virtuella datorn måste avbrytas innan den här åtgärden kan kopplas.</span><span class="sxs-lookup"><span data-stu-id="f980f-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="f980f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f980f-108">EXAMPLES</span></span>

### <span data-ttu-id="f980f-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f980f-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="f980f-110">Det här kommandot konverterar de blobbaserade diskarna för den virtuella datorn som heter ' VM01 ' i resurs gruppen ' ResourceGroup01 ' till hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="f980f-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="f980f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f980f-111">PARAMETERS</span></span>

### <span data-ttu-id="f980f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f980f-112">-AsJob</span></span>
<span data-ttu-id="f980f-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f980f-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f980f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f980f-114">-DefaultProfile</span></span>
<span data-ttu-id="f980f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f980f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f980f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f980f-116">-ResourceGroupName</span></span>
<span data-ttu-id="f980f-117">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f980f-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f980f-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="f980f-118">-VMName</span></span>
<span data-ttu-id="f980f-119">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f980f-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f980f-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f980f-120">-Confirm</span></span>
<span data-ttu-id="f980f-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f980f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f980f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f980f-122">-WhatIf</span></span>
<span data-ttu-id="f980f-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f980f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f980f-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f980f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f980f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f980f-125">CommonParameters</span></span>
<span data-ttu-id="f980f-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f980f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f980f-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f980f-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f980f-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f980f-128">INPUTS</span></span>

### <span data-ttu-id="f980f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f980f-129">System.String</span></span>

## <span data-ttu-id="f980f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f980f-130">OUTPUTS</span></span>

### <span data-ttu-id="f980f-131">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f980f-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f980f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f980f-132">NOTES</span></span>

## <span data-ttu-id="f980f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f980f-133">RELATED LINKS</span></span>
