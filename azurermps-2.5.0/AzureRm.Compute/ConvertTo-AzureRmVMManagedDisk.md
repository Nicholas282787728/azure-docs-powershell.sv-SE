---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
ms.openlocfilehash: 563b8acadcf84359af740f504f3b25555a2e45f1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930749"
---
# <span data-ttu-id="3f866-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3f866-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="3f866-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f866-102">SYNOPSIS</span></span>
<span data-ttu-id="3f866-103">Konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="3f866-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f866-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f866-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f866-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f866-105">DESCRIPTION</span></span>
<span data-ttu-id="3f866-106">**ConvertTo-AzureRmVMManagedDisk-** cmdlet konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="3f866-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="3f866-107">Den virtuella datorn måste avbrytas innan den här åtgärden kan kopplas.</span><span class="sxs-lookup"><span data-stu-id="3f866-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="3f866-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f866-108">EXAMPLES</span></span>

### <span data-ttu-id="3f866-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3f866-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="3f866-110">Det här kommandot konverterar de blobbaserade diskarna för den virtuella datorn som heter ' VM01 ' i resurs gruppen ' ResourceGroup01 ' till hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="3f866-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="3f866-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f866-111">PARAMETERS</span></span>

### <span data-ttu-id="3f866-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f866-112">-AsJob</span></span>
<span data-ttu-id="3f866-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3f866-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f866-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f866-114">-DefaultProfile</span></span>
<span data-ttu-id="3f866-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f866-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f866-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f866-116">-ResourceGroupName</span></span>
<span data-ttu-id="3f866-117">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3f866-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3f866-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="3f866-118">-VMName</span></span>
<span data-ttu-id="3f866-119">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3f866-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="3f866-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f866-120">-Confirm</span></span>
<span data-ttu-id="3f866-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f866-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f866-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f866-122">-WhatIf</span></span>
<span data-ttu-id="3f866-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f866-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f866-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f866-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f866-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f866-125">CommonParameters</span></span>
<span data-ttu-id="3f866-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f866-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f866-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f866-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f866-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f866-128">INPUTS</span></span>

### <span data-ttu-id="3f866-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3f866-129">System.String</span></span>

## <span data-ttu-id="3f866-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f866-130">OUTPUTS</span></span>

### <span data-ttu-id="3f866-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="3f866-131">System.Object</span></span>

## <span data-ttu-id="3f866-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f866-132">NOTES</span></span>

## <span data-ttu-id="3f866-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f866-133">RELATED LINKS</span></span>

