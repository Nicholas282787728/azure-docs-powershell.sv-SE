---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: 2787c1cf8a37fd5d143e95c55d3e98b625d4d82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574354"
---
# <span data-ttu-id="b55f5-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b55f5-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="b55f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b55f5-102">SYNOPSIS</span></span>
<span data-ttu-id="b55f5-103">Ger åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="b55f5-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b55f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b55f5-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b55f5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b55f5-105">DESCRIPTION</span></span>
<span data-ttu-id="b55f5-106">**Grant-AzureRmDiskAccess** cmdlet ger en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="b55f5-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="b55f5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b55f5-107">EXAMPLES</span></span>

### <span data-ttu-id="b55f5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b55f5-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="b55f5-109">Ge "Read"-åtkomst till disken med namnet "Disk01" i resurs gruppen med namnet "ResourceGroup01" för 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="b55f5-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="b55f5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b55f5-110">PARAMETERS</span></span>

### <span data-ttu-id="b55f5-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="b55f5-111">-Access</span></span>
<span data-ttu-id="b55f5-112">Anger åtkomst nivå.</span><span class="sxs-lookup"><span data-stu-id="b55f5-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55f5-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="b55f5-113">-DiskName</span></span>
<span data-ttu-id="b55f5-114">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="b55f5-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="b55f5-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="b55f5-115">-DurationInSecond</span></span>
<span data-ttu-id="b55f5-116">Anger åtkomst längd i sekunder.</span><span class="sxs-lookup"><span data-stu-id="b55f5-116">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b55f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="b55f5-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b55f5-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b55f5-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b55f5-119">-Confirm</span></span>
<span data-ttu-id="b55f5-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b55f5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b55f5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b55f5-121">-WhatIf</span></span>
<span data-ttu-id="b55f5-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b55f5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b55f5-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b55f5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b55f5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55f5-124">CommonParameters</span></span>
<span data-ttu-id="b55f5-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b55f5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55f5-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b55f5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55f5-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b55f5-127">INPUTS</span></span>

### <span data-ttu-id="b55f5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b55f5-128">System.String</span></span>

## <span data-ttu-id="b55f5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b55f5-129">OUTPUTS</span></span>

### <span data-ttu-id="b55f5-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="b55f5-130">System.Object</span></span>

## <span data-ttu-id="b55f5-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b55f5-131">NOTES</span></span>

## <span data-ttu-id="b55f5-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b55f5-132">RELATED LINKS</span></span>

