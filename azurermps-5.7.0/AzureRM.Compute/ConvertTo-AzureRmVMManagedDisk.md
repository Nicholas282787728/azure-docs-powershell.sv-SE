---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: bbfe3018cdf0560b7c7776217ceda7cfe7b77048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584440"
---
# <span data-ttu-id="a3e28-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="a3e28-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="a3e28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3e28-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e28-103">Konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="a3e28-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3e28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3e28-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3e28-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3e28-105">DESCRIPTION</span></span>
<span data-ttu-id="a3e28-106">**ConvertTo-AzureRmVMManagedDisk-** cmdlet konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="a3e28-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="a3e28-107">Den virtuella datorn måste avbrytas innan den här åtgärden kan kopplas.</span><span class="sxs-lookup"><span data-stu-id="a3e28-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="a3e28-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3e28-108">EXAMPLES</span></span>

### <span data-ttu-id="a3e28-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a3e28-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="a3e28-110">Det här kommandot konverterar de blobbaserade diskarna för den virtuella datorn som heter ' VM01 ' i resurs gruppen ' ResourceGroup01 ' till hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="a3e28-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="a3e28-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3e28-111">PARAMETERS</span></span>

### <span data-ttu-id="a3e28-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3e28-112">-ResourceGroupName</span></span>
<span data-ttu-id="a3e28-113">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a3e28-113">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3e28-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="a3e28-114">-VMName</span></span>
<span data-ttu-id="a3e28-115">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a3e28-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3e28-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3e28-116">-Confirm</span></span>
<span data-ttu-id="a3e28-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3e28-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e28-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3e28-118">-WhatIf</span></span>
<span data-ttu-id="a3e28-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3e28-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3e28-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3e28-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3e28-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e28-121">CommonParameters</span></span>
<span data-ttu-id="a3e28-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3e28-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e28-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3e28-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e28-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3e28-124">INPUTS</span></span>

### <span data-ttu-id="a3e28-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a3e28-125">System.String</span></span>

## <span data-ttu-id="a3e28-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3e28-126">OUTPUTS</span></span>

### <span data-ttu-id="a3e28-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="a3e28-127">System.Object</span></span>

## <span data-ttu-id="a3e28-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3e28-128">NOTES</span></span>

## <span data-ttu-id="a3e28-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3e28-129">RELATED LINKS</span></span>

