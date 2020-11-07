---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 4c22f8cf7ded27083ad6f1ddbd5994241d542c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924901"
---
# <span data-ttu-id="a2290-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="a2290-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="a2290-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2290-102">SYNOPSIS</span></span>
<span data-ttu-id="a2290-103">Återkallar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="a2290-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="a2290-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2290-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2290-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2290-105">DESCRIPTION</span></span>
<span data-ttu-id="a2290-106">Cmdleten **REVOKE-AzSnapshotAccess** avvisar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="a2290-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="a2290-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2290-107">EXAMPLES</span></span>

### <span data-ttu-id="a2290-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2290-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="a2290-109">Återkalla åtkomsten till ögonblicks bilden med namnet "Snapshot01" i resurs gruppen med namnet "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="a2290-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="a2290-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2290-110">PARAMETERS</span></span>

### <span data-ttu-id="a2290-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2290-111">-AsJob</span></span>
<span data-ttu-id="a2290-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a2290-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2290-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2290-113">-DefaultProfile</span></span>
<span data-ttu-id="a2290-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2290-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2290-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2290-115">-ResourceGroupName</span></span>
<span data-ttu-id="a2290-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a2290-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a2290-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="a2290-117">-SnapshotName</span></span>
<span data-ttu-id="a2290-118">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="a2290-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="a2290-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2290-119">-Confirm</span></span>
<span data-ttu-id="a2290-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2290-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2290-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2290-121">-WhatIf</span></span>
<span data-ttu-id="a2290-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2290-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2290-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2290-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2290-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2290-124">CommonParameters</span></span>
<span data-ttu-id="a2290-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2290-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2290-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2290-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2290-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2290-127">INPUTS</span></span>

### <span data-ttu-id="a2290-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a2290-128">System.String</span></span>

## <span data-ttu-id="a2290-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2290-129">OUTPUTS</span></span>

### <span data-ttu-id="a2290-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="a2290-130">System.Object</span></span>

## <span data-ttu-id="a2290-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2290-131">NOTES</span></span>

## <span data-ttu-id="a2290-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2290-132">RELATED LINKS</span></span>

