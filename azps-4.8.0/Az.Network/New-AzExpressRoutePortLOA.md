---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262586"
---
# <span data-ttu-id="09f07-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="09f07-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="09f07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09f07-102">SYNOPSIS</span></span>
<span data-ttu-id="09f07-103">Ladda ned rem bur handlingen för en Express-vägs port.</span><span class="sxs-lookup"><span data-stu-id="09f07-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="09f07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09f07-104">SYNTAX</span></span>

### <span data-ttu-id="09f07-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="09f07-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f07-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09f07-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f07-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09f07-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09f07-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09f07-108">DESCRIPTION</span></span>
<span data-ttu-id="09f07-109">New-AzExpressRoutePortLOA cmdlet laddar ned ett brev i PDF-format för en Express-vägs port.</span><span class="sxs-lookup"><span data-stu-id="09f07-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="09f07-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09f07-110">EXAMPLES</span></span>

### <span data-ttu-id="09f07-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="09f07-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="09f07-112">Hämta rem bur handlingen för Express Route port "min port" och lagra den i filen "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="09f07-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="09f07-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09f07-113">PARAMETERS</span></span>

### <span data-ttu-id="09f07-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09f07-114">-AsJob</span></span>
<span data-ttu-id="09f07-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="09f07-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09f07-116">-Kundnamn</span><span class="sxs-lookup"><span data-stu-id="09f07-116">-CustomerName</span></span>
<span data-ttu-id="09f07-117">Kund namnet som den här Express flödes porten är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="09f07-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f07-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f07-118">-DefaultProfile</span></span>
<span data-ttu-id="09f07-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09f07-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09f07-120">-Mål</span><span class="sxs-lookup"><span data-stu-id="09f07-120">-Destination</span></span>
<span data-ttu-id="09f07-121">Utgångs filen som ska spara godkännande brevet.</span><span class="sxs-lookup"><span data-stu-id="09f07-121">The output filepath to store the Letter of Authorization to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f07-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="09f07-122">-ExpressRoutePort</span></span>
<span data-ttu-id="09f07-123">Resursen ExpressRoute port.</span><span class="sxs-lookup"><span data-stu-id="09f07-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f07-124">-ID</span><span class="sxs-lookup"><span data-stu-id="09f07-124">-Id</span></span>
<span data-ttu-id="09f07-125">ResourceId för ExpressRoute-porten.</span><span class="sxs-lookup"><span data-stu-id="09f07-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f07-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09f07-126">-PassThru</span></span>
<span data-ttu-id="09f07-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="09f07-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="09f07-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="09f07-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="09f07-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="09f07-129">-PortName</span></span>
<span data-ttu-id="09f07-130">Namnet på ExpressRoute-vägen.</span><span class="sxs-lookup"><span data-stu-id="09f07-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f07-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f07-131">-ResourceGroupName</span></span>
<span data-ttu-id="09f07-132">Namnet på den uttryckliga vägen i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="09f07-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f07-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f07-133">CommonParameters</span></span>
<span data-ttu-id="09f07-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f07-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f07-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09f07-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f07-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09f07-136">INPUTS</span></span>

### <span data-ttu-id="09f07-137">System. String</span><span class="sxs-lookup"><span data-stu-id="09f07-137">System.String</span></span>

## <span data-ttu-id="09f07-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09f07-138">OUTPUTS</span></span>

### <span data-ttu-id="09f07-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09f07-139">System.Boolean</span></span>

## <span data-ttu-id="09f07-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09f07-140">NOTES</span></span>

## <span data-ttu-id="09f07-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09f07-141">RELATED LINKS</span></span>
