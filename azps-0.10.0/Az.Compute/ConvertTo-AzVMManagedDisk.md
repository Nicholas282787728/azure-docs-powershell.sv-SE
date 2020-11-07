---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 882b9f0afe9670f9e7b6f0651b3f3a96003d4668
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925254"
---
# <span data-ttu-id="1b1bf-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1b1bf-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="1b1bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b1bf-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1bf-103">Konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="1b1bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b1bf-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b1bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b1bf-105">DESCRIPTION</span></span>
<span data-ttu-id="1b1bf-106">**ConvertTo-AzVMManagedDisk-** cmdlet konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="1b1bf-107">Den virtuella datorn måste avbrytas innan den här åtgärden kan kopplas.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="1b1bf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b1bf-108">EXAMPLES</span></span>

### <span data-ttu-id="1b1bf-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1b1bf-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="1b1bf-110">Det här kommandot konverterar de blobbaserade diskarna för den virtuella datorn som heter ' VM01 ' i resurs gruppen ' ResourceGroup01 ' till hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="1b1bf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b1bf-111">PARAMETERS</span></span>

### <span data-ttu-id="1b1bf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b1bf-112">-AsJob</span></span>
<span data-ttu-id="1b1bf-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1b1bf-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b1bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1bf-114">-DefaultProfile</span></span>
<span data-ttu-id="1b1bf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b1bf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1bf-116">-ResourceGroupName</span></span>
<span data-ttu-id="1b1bf-117">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1b1bf-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="1b1bf-118">-VMName</span></span>
<span data-ttu-id="1b1bf-119">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="1b1bf-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b1bf-120">-Confirm</span></span>
<span data-ttu-id="1b1bf-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b1bf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b1bf-122">-WhatIf</span></span>
<span data-ttu-id="1b1bf-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b1bf-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b1bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1bf-125">CommonParameters</span></span>
<span data-ttu-id="1b1bf-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1bf-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b1bf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1bf-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b1bf-128">INPUTS</span></span>

### <span data-ttu-id="1b1bf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1b1bf-129">System.String</span></span>

## <span data-ttu-id="1b1bf-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b1bf-130">OUTPUTS</span></span>

### <span data-ttu-id="1b1bf-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="1b1bf-131">System.Object</span></span>

## <span data-ttu-id="1b1bf-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b1bf-132">NOTES</span></span>

## <span data-ttu-id="1b1bf-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b1bf-133">RELATED LINKS</span></span>

