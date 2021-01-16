---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 66c91c7a486638c01902f6091993143bb2e1a535
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417584"
---
# <span data-ttu-id="9cb6e-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9cb6e-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="9cb6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb6e-103">Konfigurerar en ny Edge-enhet</span><span class="sxs-lookup"><span data-stu-id="9cb6e-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="9cb6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cb6e-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cb6e-105">DESCRIPTION</span></span>
<span data-ttu-id="9cb6e-106">Cmdleten **New-AzDataBoxEdgeDevice** konfigurerar en ny Edge-enhet för data ruta</span><span class="sxs-lookup"><span data-stu-id="9cb6e-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="9cb6e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cb6e-107">EXAMPLES</span></span>

### <span data-ttu-id="9cb6e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9cb6e-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="9cb6e-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cb6e-109">PARAMETERS</span></span>

### <span data-ttu-id="9cb6e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cb6e-110">-AsJob</span></span>
<span data-ttu-id="9cb6e-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9cb6e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cb6e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb6e-112">-DefaultProfile</span></span>
<span data-ttu-id="9cb6e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb6e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb6e-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="9cb6e-114">-Location</span></span>
<span data-ttu-id="9cb6e-115">Enhetens plats</span><span class="sxs-lookup"><span data-stu-id="9cb6e-115">Location of the device</span></span>

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

### <span data-ttu-id="9cb6e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="9cb6e-116">-Name</span></span>
<span data-ttu-id="9cb6e-117">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="9cb6e-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb6e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb6e-118">-ResourceGroupName</span></span>
<span data-ttu-id="9cb6e-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9cb6e-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cb6e-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="9cb6e-120">-Sku</span></span>
<span data-ttu-id="9cb6e-121">Tillgängliga SKU: er är Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="9cb6e-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="9cb6e-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9cb6e-122">-Confirm</span></span>
<span data-ttu-id="9cb6e-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cb6e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb6e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb6e-124">-WhatIf</span></span>
<span data-ttu-id="9cb6e-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9cb6e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cb6e-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9cb6e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb6e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb6e-127">CommonParameters</span></span>
<span data-ttu-id="9cb6e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb6e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb6e-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cb6e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb6e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cb6e-130">INPUTS</span></span>

### <span data-ttu-id="9cb6e-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="9cb6e-131">None</span></span>

## <span data-ttu-id="9cb6e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cb6e-132">OUTPUTS</span></span>

### <span data-ttu-id="9cb6e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9cb6e-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="9cb6e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cb6e-134">NOTES</span></span>

## <span data-ttu-id="9cb6e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cb6e-135">RELATED LINKS</span></span>
