---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522937"
---
# <span data-ttu-id="cd751-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cd751-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="cd751-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd751-102">SYNOPSIS</span></span>
<span data-ttu-id="cd751-103">Konfigurerar en ny Trave</span><span class="sxs-lookup"><span data-stu-id="cd751-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="cd751-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd751-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd751-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd751-105">DESCRIPTION</span></span>
<span data-ttu-id="cd751-106">Cmdleten **New-AzStackEdgeDevice** konfigurerar en ny Trave</span><span class="sxs-lookup"><span data-stu-id="cd751-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="cd751-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd751-107">EXAMPLES</span></span>

### <span data-ttu-id="cd751-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd751-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="cd751-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd751-109">PARAMETERS</span></span>

### <span data-ttu-id="cd751-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd751-110">-AsJob</span></span>
<span data-ttu-id="cd751-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cd751-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd751-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd751-112">-DefaultProfile</span></span>
<span data-ttu-id="cd751-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd751-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd751-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="cd751-114">-Location</span></span>
<span data-ttu-id="cd751-115">Enhetens plats</span><span class="sxs-lookup"><span data-stu-id="cd751-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd751-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd751-116">-Name</span></span>
<span data-ttu-id="cd751-117">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="cd751-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd751-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd751-118">-ResourceGroupName</span></span>
<span data-ttu-id="cd751-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="cd751-119">Resource Group Name</span></span>

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

### <span data-ttu-id="cd751-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="cd751-120">-Sku</span></span>
<span data-ttu-id="cd751-121">Tillgängliga SKU: er är Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="cd751-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd751-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd751-122">-Confirm</span></span>
<span data-ttu-id="cd751-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd751-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd751-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd751-124">-WhatIf</span></span>
<span data-ttu-id="cd751-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd751-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd751-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd751-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd751-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd751-127">CommonParameters</span></span>
<span data-ttu-id="cd751-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd751-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd751-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd751-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd751-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd751-130">INPUTS</span></span>

### <span data-ttu-id="cd751-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd751-131">None</span></span>

## <span data-ttu-id="cd751-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd751-132">OUTPUTS</span></span>

### <span data-ttu-id="cd751-133">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cd751-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="cd751-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd751-134">NOTES</span></span>

## <span data-ttu-id="cd751-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd751-135">RELATED LINKS</span></span>
