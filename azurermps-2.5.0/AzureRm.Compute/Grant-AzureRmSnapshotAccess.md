---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: b1957543c959a18c9fd0fe4fc12de02064ffdcf0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930346"
---
# <span data-ttu-id="eb11e-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="eb11e-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="eb11e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb11e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb11e-103">Ger åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="eb11e-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb11e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb11e-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb11e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb11e-105">DESCRIPTION</span></span>
<span data-ttu-id="eb11e-106">**Grant-AzureRmSnapshotAccess** cmdlet beviljar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="eb11e-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="eb11e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb11e-107">EXAMPLES</span></span>

### <span data-ttu-id="eb11e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb11e-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="eb11e-109">Ge "Read"-åtkomst till ögonblicks bilden med namnet "Snapshot01" i resurs gruppen med namnet "ResourceGroup01" för 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="eb11e-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="eb11e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb11e-110">PARAMETERS</span></span>

### <span data-ttu-id="eb11e-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="eb11e-111">-Access</span></span>
<span data-ttu-id="eb11e-112">Anger åtkomst nivå.</span><span class="sxs-lookup"><span data-stu-id="eb11e-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="eb11e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb11e-113">-AsJob</span></span>
<span data-ttu-id="eb11e-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eb11e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb11e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb11e-115">-DefaultProfile</span></span>
<span data-ttu-id="eb11e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb11e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb11e-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="eb11e-117">-DurationInSecond</span></span>
<span data-ttu-id="eb11e-118">Anger åtkomst längd i sekunder.</span><span class="sxs-lookup"><span data-stu-id="eb11e-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="eb11e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb11e-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb11e-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="eb11e-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eb11e-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="eb11e-121">-SnapshotName</span></span>
<span data-ttu-id="eb11e-122">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="eb11e-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="eb11e-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb11e-123">-Confirm</span></span>
<span data-ttu-id="eb11e-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb11e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb11e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb11e-125">-WhatIf</span></span>
<span data-ttu-id="eb11e-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb11e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb11e-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb11e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb11e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb11e-128">CommonParameters</span></span>
<span data-ttu-id="eb11e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb11e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb11e-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb11e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb11e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb11e-131">INPUTS</span></span>

### <span data-ttu-id="eb11e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="eb11e-132">System.String</span></span>

## <span data-ttu-id="eb11e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb11e-133">OUTPUTS</span></span>

### <span data-ttu-id="eb11e-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="eb11e-134">System.Object</span></span>

## <span data-ttu-id="eb11e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb11e-135">NOTES</span></span>

## <span data-ttu-id="eb11e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb11e-136">RELATED LINKS</span></span>

