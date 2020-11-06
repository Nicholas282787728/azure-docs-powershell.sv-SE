---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 6931f6d80d3e279259b599b782a505b2a21dd074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585779"
---
# <span data-ttu-id="1d3db-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1d3db-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="1d3db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d3db-102">SYNOPSIS</span></span>
<span data-ttu-id="1d3db-103">Konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="1d3db-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d3db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d3db-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d3db-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d3db-105">DESCRIPTION</span></span>
<span data-ttu-id="1d3db-106">**ConvertTo-AzureRmVMManagedDisk-** cmdlet konverterar en virtuell dator med blobbbaserade diskar till en virtuell dator med hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="1d3db-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="1d3db-107">Den virtuella datorn måste avbrytas innan den här åtgärden kan kopplas.</span><span class="sxs-lookup"><span data-stu-id="1d3db-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="1d3db-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d3db-108">EXAMPLES</span></span>

### <span data-ttu-id="1d3db-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1d3db-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="1d3db-110">Det här kommandot konverterar de blobbaserade diskarna för den virtuella datorn som heter ' VM01 ' i resurs gruppen ' ResourceGroup01 ' till hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="1d3db-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="1d3db-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d3db-111">PARAMETERS</span></span>

### <span data-ttu-id="1d3db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d3db-112">-DefaultProfile</span></span>
<span data-ttu-id="1d3db-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1d3db-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d3db-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d3db-114">-ResourceGroupName</span></span>
<span data-ttu-id="1d3db-115">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1d3db-115">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d3db-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="1d3db-116">-VMName</span></span>
<span data-ttu-id="1d3db-117">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="1d3db-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d3db-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1d3db-118">-Confirm</span></span>
<span data-ttu-id="1d3db-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1d3db-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d3db-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d3db-120">-WhatIf</span></span>
<span data-ttu-id="1d3db-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1d3db-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d3db-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1d3db-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d3db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d3db-123">CommonParameters</span></span>
<span data-ttu-id="1d3db-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d3db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d3db-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d3db-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d3db-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d3db-126">INPUTS</span></span>

### <span data-ttu-id="1d3db-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1d3db-127">System.String</span></span>

## <span data-ttu-id="1d3db-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d3db-128">OUTPUTS</span></span>

### <span data-ttu-id="1d3db-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="1d3db-129">System.Object</span></span>

## <span data-ttu-id="1d3db-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d3db-130">NOTES</span></span>

## <span data-ttu-id="1d3db-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d3db-131">RELATED LINKS</span></span>

