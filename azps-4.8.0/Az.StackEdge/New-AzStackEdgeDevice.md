---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261552"
---
# <span data-ttu-id="b0394-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b0394-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="b0394-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0394-102">SYNOPSIS</span></span>
<span data-ttu-id="b0394-103">Konfigurerar en ny Trave</span><span class="sxs-lookup"><span data-stu-id="b0394-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="b0394-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0394-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0394-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0394-105">DESCRIPTION</span></span>
<span data-ttu-id="b0394-106">Cmdleten **New-AzStackEdgeDevice** konfigurerar en ny Trave</span><span class="sxs-lookup"><span data-stu-id="b0394-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="b0394-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0394-107">EXAMPLES</span></span>

### <span data-ttu-id="b0394-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b0394-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="b0394-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0394-109">PARAMETERS</span></span>

### <span data-ttu-id="b0394-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0394-110">-AsJob</span></span>
<span data-ttu-id="b0394-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b0394-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0394-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0394-112">-DefaultProfile</span></span>
<span data-ttu-id="b0394-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0394-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0394-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="b0394-114">-Location</span></span>
<span data-ttu-id="b0394-115">Enhetens plats</span><span class="sxs-lookup"><span data-stu-id="b0394-115">Location of the device</span></span>

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

### <span data-ttu-id="b0394-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0394-116">-Name</span></span>
<span data-ttu-id="b0394-117">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="b0394-117">Resource Name</span></span>

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

### <span data-ttu-id="b0394-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0394-118">-ResourceGroupName</span></span>
<span data-ttu-id="b0394-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b0394-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b0394-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="b0394-120">-Sku</span></span>
<span data-ttu-id="b0394-121">Tillgängliga SKU: er är Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="b0394-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="b0394-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0394-122">-Confirm</span></span>
<span data-ttu-id="b0394-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0394-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0394-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0394-124">-WhatIf</span></span>
<span data-ttu-id="b0394-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0394-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0394-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0394-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0394-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0394-127">CommonParameters</span></span>
<span data-ttu-id="b0394-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0394-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0394-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0394-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0394-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0394-130">INPUTS</span></span>

### <span data-ttu-id="b0394-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="b0394-131">None</span></span>

## <span data-ttu-id="b0394-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0394-132">OUTPUTS</span></span>

### <span data-ttu-id="b0394-133">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b0394-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="b0394-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0394-134">NOTES</span></span>

## <span data-ttu-id="b0394-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0394-135">RELATED LINKS</span></span>
