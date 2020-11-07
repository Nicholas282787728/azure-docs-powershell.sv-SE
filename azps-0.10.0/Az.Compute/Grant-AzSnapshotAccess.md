---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: e4283b23fb4a82c17f35354d854c30c3ec1b2329
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925101"
---
# <span data-ttu-id="c9d21-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c9d21-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="c9d21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9d21-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d21-103">Ger åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="c9d21-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="c9d21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9d21-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9d21-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9d21-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d21-106">**Grant-AzSnapshotAccess** cmdlet beviljar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="c9d21-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="c9d21-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9d21-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d21-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c9d21-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="c9d21-109">Ge "Read"-åtkomst till ögonblicks bilden med namnet "Snapshot01" i resurs gruppen med namnet "ResourceGroup01" för 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="c9d21-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="c9d21-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9d21-110">PARAMETERS</span></span>

### <span data-ttu-id="c9d21-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="c9d21-111">-Access</span></span>
<span data-ttu-id="c9d21-112">Anger åtkomst nivå.</span><span class="sxs-lookup"><span data-stu-id="c9d21-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="c9d21-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9d21-113">-AsJob</span></span>
<span data-ttu-id="c9d21-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c9d21-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9d21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d21-115">-DefaultProfile</span></span>
<span data-ttu-id="c9d21-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d21-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d21-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="c9d21-117">-DurationInSecond</span></span>
<span data-ttu-id="c9d21-118">Anger åtkomst längd i sekunder.</span><span class="sxs-lookup"><span data-stu-id="c9d21-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="c9d21-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d21-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9d21-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c9d21-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c9d21-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="c9d21-121">-SnapshotName</span></span>
<span data-ttu-id="c9d21-122">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="c9d21-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="c9d21-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c9d21-123">-Confirm</span></span>
<span data-ttu-id="c9d21-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c9d21-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d21-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d21-125">-WhatIf</span></span>
<span data-ttu-id="c9d21-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c9d21-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9d21-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c9d21-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d21-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d21-128">CommonParameters</span></span>
<span data-ttu-id="c9d21-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d21-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d21-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d21-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d21-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9d21-131">INPUTS</span></span>

### <span data-ttu-id="c9d21-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c9d21-132">System.String</span></span>

## <span data-ttu-id="c9d21-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9d21-133">OUTPUTS</span></span>

### <span data-ttu-id="c9d21-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="c9d21-134">System.Object</span></span>

## <span data-ttu-id="c9d21-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9d21-135">NOTES</span></span>

## <span data-ttu-id="c9d21-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9d21-136">RELATED LINKS</span></span>

