---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: eb71d1a74e68bdf4157cacd4b87aa9a05bdc00db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572887"
---
# <span data-ttu-id="63cc8-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="63cc8-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="63cc8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="63cc8-103">Återkallar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="63cc8-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63cc8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63cc8-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63cc8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63cc8-105">DESCRIPTION</span></span>
<span data-ttu-id="63cc8-106">Cmdleten **REVOKE-AzureRmSnapshotAccess** avvisar en åtkomst till en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="63cc8-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="63cc8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63cc8-107">EXAMPLES</span></span>

### <span data-ttu-id="63cc8-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63cc8-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="63cc8-109">Återkalla åtkomsten till ögonblicks bilden med namnet "Snapshot01" i resurs gruppen med namnet "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="63cc8-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="63cc8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63cc8-110">PARAMETERS</span></span>

### <span data-ttu-id="63cc8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63cc8-111">-AsJob</span></span>
<span data-ttu-id="63cc8-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="63cc8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63cc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63cc8-113">-DefaultProfile</span></span>
<span data-ttu-id="63cc8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63cc8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63cc8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63cc8-115">-ResourceGroupName</span></span>
<span data-ttu-id="63cc8-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="63cc8-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="63cc8-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="63cc8-117">-SnapshotName</span></span>
<span data-ttu-id="63cc8-118">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="63cc8-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="63cc8-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63cc8-119">-Confirm</span></span>
<span data-ttu-id="63cc8-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63cc8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63cc8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63cc8-121">-WhatIf</span></span>
<span data-ttu-id="63cc8-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63cc8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63cc8-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63cc8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63cc8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63cc8-124">CommonParameters</span></span>
<span data-ttu-id="63cc8-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63cc8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63cc8-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63cc8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63cc8-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63cc8-127">INPUTS</span></span>

### <span data-ttu-id="63cc8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="63cc8-128">System.String</span></span>

## <span data-ttu-id="63cc8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63cc8-129">OUTPUTS</span></span>

### <span data-ttu-id="63cc8-130">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="63cc8-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="63cc8-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63cc8-131">NOTES</span></span>

## <span data-ttu-id="63cc8-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63cc8-132">RELATED LINKS</span></span>
