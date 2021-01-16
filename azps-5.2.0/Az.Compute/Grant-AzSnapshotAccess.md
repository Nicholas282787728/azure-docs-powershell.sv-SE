---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394000"
---
# <span data-ttu-id="fd477-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="fd477-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="fd477-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd477-102">SYNOPSIS</span></span>
<span data-ttu-id="fd477-103">Ger åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fd477-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="fd477-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd477-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd477-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd477-105">DESCRIPTION</span></span>
<span data-ttu-id="fd477-106">**Grant-AzSnapshotAccess** cmdlet beviljar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fd477-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="fd477-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd477-107">EXAMPLES</span></span>

### <span data-ttu-id="fd477-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fd477-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="fd477-109">Ge "Read"-åtkomst till ögonblicks bilden med namnet "Snapshot01" i resurs gruppen med namnet "ResourceGroup01" för 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="fd477-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="fd477-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd477-110">PARAMETERS</span></span>

### <span data-ttu-id="fd477-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="fd477-111">-Access</span></span>
<span data-ttu-id="fd477-112">Anger åtkomst nivå.</span><span class="sxs-lookup"><span data-stu-id="fd477-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd477-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd477-113">-AsJob</span></span>
<span data-ttu-id="fd477-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="fd477-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd477-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd477-115">-DefaultProfile</span></span>
<span data-ttu-id="fd477-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd477-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd477-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="fd477-117">-DurationInSecond</span></span>
<span data-ttu-id="fd477-118">Anger åtkomst längd i sekunder.</span><span class="sxs-lookup"><span data-stu-id="fd477-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd477-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd477-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd477-120">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fd477-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fd477-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="fd477-121">-SnapshotName</span></span>
<span data-ttu-id="fd477-122">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fd477-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="fd477-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd477-123">-Confirm</span></span>
<span data-ttu-id="fd477-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd477-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd477-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd477-125">-WhatIf</span></span>
<span data-ttu-id="fd477-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd477-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd477-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd477-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd477-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd477-128">CommonParameters</span></span>
<span data-ttu-id="fd477-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd477-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd477-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd477-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd477-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd477-131">INPUTS</span></span>

### <span data-ttu-id="fd477-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fd477-132">System.String</span></span>

## <span data-ttu-id="fd477-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd477-133">OUTPUTS</span></span>

### <span data-ttu-id="fd477-134">Microsoft. Azure. commands. Compute. Automation. Models. PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="fd477-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="fd477-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd477-135">NOTES</span></span>

## <span data-ttu-id="fd477-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd477-136">RELATED LINKS</span></span>
