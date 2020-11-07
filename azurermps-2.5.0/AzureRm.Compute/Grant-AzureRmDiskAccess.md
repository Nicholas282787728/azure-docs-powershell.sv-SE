---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: c574b273082d3c7e840d589fe765190d99028d89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930349"
---
# <span data-ttu-id="9b5ba-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="9b5ba-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="9b5ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5ba-103">Ger åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b5ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b5ba-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b5ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b5ba-105">DESCRIPTION</span></span>
<span data-ttu-id="9b5ba-106">**Grant-AzureRmDiskAccess** cmdlet ger en åtkomst till en disk.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="9b5ba-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b5ba-107">EXAMPLES</span></span>

### <span data-ttu-id="9b5ba-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b5ba-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="9b5ba-109">Ge "Read"-åtkomst till disken med namnet "Disk01" i resurs gruppen med namnet "ResourceGroup01" för 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="9b5ba-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b5ba-110">PARAMETERS</span></span>

### <span data-ttu-id="9b5ba-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="9b5ba-111">-Access</span></span>
<span data-ttu-id="9b5ba-112">Anger åtkomst nivå.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5ba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b5ba-113">-AsJob</span></span>
<span data-ttu-id="9b5ba-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9b5ba-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b5ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5ba-115">-DefaultProfile</span></span>
<span data-ttu-id="9b5ba-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b5ba-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="9b5ba-117">-DiskName</span></span>
<span data-ttu-id="9b5ba-118">Anger namnet på en disk.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="9b5ba-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="9b5ba-119">-DurationInSecond</span></span>
<span data-ttu-id="9b5ba-120">Anger åtkomst längd i sekunder.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="9b5ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b5ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b5ba-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9b5ba-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b5ba-123">-Confirm</span></span>
<span data-ttu-id="9b5ba-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b5ba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5ba-125">-WhatIf</span></span>
<span data-ttu-id="9b5ba-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b5ba-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b5ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5ba-128">CommonParameters</span></span>
<span data-ttu-id="9b5ba-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b5ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5ba-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b5ba-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5ba-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b5ba-131">INPUTS</span></span>

### <span data-ttu-id="9b5ba-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9b5ba-132">System.String</span></span>

## <span data-ttu-id="9b5ba-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b5ba-133">OUTPUTS</span></span>

### <span data-ttu-id="9b5ba-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="9b5ba-134">System.Object</span></span>

## <span data-ttu-id="9b5ba-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b5ba-135">NOTES</span></span>

## <span data-ttu-id="9b5ba-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b5ba-136">RELATED LINKS</span></span>

