---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: 9b870214362c6e2bcd7225ef5a40ed5ff780139a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577696"
---
# <span data-ttu-id="75964-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="75964-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="75964-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75964-102">SYNOPSIS</span></span>
<span data-ttu-id="75964-103">Ger åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="75964-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75964-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75964-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75964-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75964-105">DESCRIPTION</span></span>
<span data-ttu-id="75964-106">**Grant-AzureRmSnapshotAccess** cmdlet beviljar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="75964-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="75964-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75964-107">EXAMPLES</span></span>

### <span data-ttu-id="75964-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="75964-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="75964-109">Ge "Read"-åtkomst till ögonblicks bilden med namnet "Snapshot01" i resurs gruppen med namnet "ResourceGroup01" för 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="75964-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="75964-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75964-110">PARAMETERS</span></span>

### <span data-ttu-id="75964-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="75964-111">-Access</span></span>
<span data-ttu-id="75964-112">Anger åtkomst nivå.</span><span class="sxs-lookup"><span data-stu-id="75964-112">Specifies Access level.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75964-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75964-113">-DefaultProfile</span></span>
<span data-ttu-id="75964-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75964-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75964-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="75964-115">-DurationInSecond</span></span>
<span data-ttu-id="75964-116">Anger åtkomst längd i sekunder.</span><span class="sxs-lookup"><span data-stu-id="75964-116">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75964-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75964-117">-ResourceGroupName</span></span>
<span data-ttu-id="75964-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="75964-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="75964-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="75964-119">-SnapshotName</span></span>
<span data-ttu-id="75964-120">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="75964-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="75964-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75964-121">-Confirm</span></span>
<span data-ttu-id="75964-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75964-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75964-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75964-123">-WhatIf</span></span>
<span data-ttu-id="75964-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75964-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75964-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75964-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75964-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75964-126">CommonParameters</span></span>
<span data-ttu-id="75964-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75964-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75964-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75964-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75964-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75964-129">INPUTS</span></span>

### <span data-ttu-id="75964-130">System. String</span><span class="sxs-lookup"><span data-stu-id="75964-130">System.String</span></span>

## <span data-ttu-id="75964-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75964-131">OUTPUTS</span></span>

### <span data-ttu-id="75964-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="75964-132">System.Object</span></span>

## <span data-ttu-id="75964-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75964-133">NOTES</span></span>

## <span data-ttu-id="75964-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75964-134">RELATED LINKS</span></span>

