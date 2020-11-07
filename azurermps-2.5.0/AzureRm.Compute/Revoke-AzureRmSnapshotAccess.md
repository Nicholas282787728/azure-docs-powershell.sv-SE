---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: bbde391c56d4b50320f15441b75b93d125771ccb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931493"
---
# <span data-ttu-id="016c3-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="016c3-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="016c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="016c3-102">SYNOPSIS</span></span>
<span data-ttu-id="016c3-103">Återkallar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="016c3-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="016c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="016c3-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="016c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="016c3-105">DESCRIPTION</span></span>
<span data-ttu-id="016c3-106">Cmdleten **REVOKE-AzureRmSnapshotAccess** avvisar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="016c3-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="016c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="016c3-107">EXAMPLES</span></span>

### <span data-ttu-id="016c3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="016c3-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="016c3-109">Återkalla åtkomsten till ögonblicks bilden med namnet "Snapshot01" i resurs gruppen med namnet "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="016c3-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="016c3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="016c3-110">PARAMETERS</span></span>

### <span data-ttu-id="016c3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="016c3-111">-AsJob</span></span>
<span data-ttu-id="016c3-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="016c3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="016c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="016c3-113">-DefaultProfile</span></span>
<span data-ttu-id="016c3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="016c3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="016c3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="016c3-115">-ResourceGroupName</span></span>
<span data-ttu-id="016c3-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="016c3-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="016c3-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="016c3-117">-SnapshotName</span></span>
<span data-ttu-id="016c3-118">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="016c3-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="016c3-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="016c3-119">-Confirm</span></span>
<span data-ttu-id="016c3-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="016c3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="016c3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="016c3-121">-WhatIf</span></span>
<span data-ttu-id="016c3-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="016c3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="016c3-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="016c3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="016c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="016c3-124">CommonParameters</span></span>
<span data-ttu-id="016c3-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="016c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="016c3-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="016c3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="016c3-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="016c3-127">INPUTS</span></span>

### <span data-ttu-id="016c3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="016c3-128">System.String</span></span>

## <span data-ttu-id="016c3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="016c3-129">OUTPUTS</span></span>

### <span data-ttu-id="016c3-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="016c3-130">System.Object</span></span>

## <span data-ttu-id="016c3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="016c3-131">NOTES</span></span>

## <span data-ttu-id="016c3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="016c3-132">RELATED LINKS</span></span>

