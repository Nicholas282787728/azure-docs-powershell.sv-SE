---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263329"
---
# <span data-ttu-id="5547d-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5547d-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="5547d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5547d-102">SYNOPSIS</span></span>
<span data-ttu-id="5547d-103">Återkallar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="5547d-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="5547d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5547d-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5547d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5547d-105">DESCRIPTION</span></span>
<span data-ttu-id="5547d-106">Cmdleten **REVOKE-AzSnapshotAccess** avvisar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="5547d-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="5547d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5547d-107">EXAMPLES</span></span>

### <span data-ttu-id="5547d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5547d-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="5547d-109">Återkalla åtkomsten till ögonblicks bilden med namnet "Snapshot01" i resurs gruppen med namnet "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="5547d-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="5547d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5547d-110">PARAMETERS</span></span>

### <span data-ttu-id="5547d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5547d-111">-AsJob</span></span>
<span data-ttu-id="5547d-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5547d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5547d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5547d-113">-DefaultProfile</span></span>
<span data-ttu-id="5547d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5547d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5547d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5547d-115">-ResourceGroupName</span></span>
<span data-ttu-id="5547d-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5547d-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5547d-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="5547d-117">-SnapshotName</span></span>
<span data-ttu-id="5547d-118">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="5547d-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="5547d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5547d-119">-Confirm</span></span>
<span data-ttu-id="5547d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5547d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5547d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5547d-121">-WhatIf</span></span>
<span data-ttu-id="5547d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5547d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5547d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5547d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5547d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5547d-124">CommonParameters</span></span>
<span data-ttu-id="5547d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5547d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5547d-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5547d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5547d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5547d-127">INPUTS</span></span>

### <span data-ttu-id="5547d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5547d-128">System.String</span></span>

## <span data-ttu-id="5547d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5547d-129">OUTPUTS</span></span>

### <span data-ttu-id="5547d-130">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="5547d-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5547d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5547d-131">NOTES</span></span>

## <span data-ttu-id="5547d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5547d-132">RELATED LINKS</span></span>