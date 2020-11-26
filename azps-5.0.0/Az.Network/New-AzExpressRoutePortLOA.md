---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324635"
---
# <span data-ttu-id="40cdc-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="40cdc-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="40cdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="40cdc-103">Ladda ned rem bur handlingen för en Express-vägs port.</span><span class="sxs-lookup"><span data-stu-id="40cdc-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="40cdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40cdc-104">SYNTAX</span></span>

### <span data-ttu-id="40cdc-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="40cdc-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40cdc-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40cdc-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40cdc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40cdc-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40cdc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40cdc-108">DESCRIPTION</span></span>
<span data-ttu-id="40cdc-109">New-AzExpressRoutePortLOA cmdlet laddar ned ett brev i PDF-format för en Express-vägs port.</span><span class="sxs-lookup"><span data-stu-id="40cdc-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="40cdc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40cdc-110">EXAMPLES</span></span>

### <span data-ttu-id="40cdc-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40cdc-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="40cdc-112">Hämta rem bur handlingen för Express Route port "min port" och lagra den i filen "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="40cdc-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="40cdc-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40cdc-113">PARAMETERS</span></span>

### <span data-ttu-id="40cdc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40cdc-114">-AsJob</span></span>
<span data-ttu-id="40cdc-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="40cdc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40cdc-116">-Kundnamn</span><span class="sxs-lookup"><span data-stu-id="40cdc-116">-CustomerName</span></span>
<span data-ttu-id="40cdc-117">Kund namnet som den här Express flödes porten är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="40cdc-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="40cdc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40cdc-118">-DefaultProfile</span></span>
<span data-ttu-id="40cdc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40cdc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40cdc-120">-Mål</span><span class="sxs-lookup"><span data-stu-id="40cdc-120">-Destination</span></span>
<span data-ttu-id="40cdc-121">Utgångs filen som ska spara godkännande brevet.</span><span class="sxs-lookup"><span data-stu-id="40cdc-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="40cdc-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="40cdc-122">-ExpressRoutePort</span></span>
<span data-ttu-id="40cdc-123">Resursen ExpressRoute port.</span><span class="sxs-lookup"><span data-stu-id="40cdc-123">The express route port resource.</span></span>

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

### <span data-ttu-id="40cdc-124">-ID</span><span class="sxs-lookup"><span data-stu-id="40cdc-124">-Id</span></span>
<span data-ttu-id="40cdc-125">ResourceId för ExpressRoute-porten.</span><span class="sxs-lookup"><span data-stu-id="40cdc-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="40cdc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40cdc-126">-PassThru</span></span>
<span data-ttu-id="40cdc-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="40cdc-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="40cdc-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="40cdc-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="40cdc-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="40cdc-129">-PortName</span></span>
<span data-ttu-id="40cdc-130">Namnet på ExpressRoute-vägen.</span><span class="sxs-lookup"><span data-stu-id="40cdc-130">The express route port name.</span></span>

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

### <span data-ttu-id="40cdc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40cdc-131">-ResourceGroupName</span></span>
<span data-ttu-id="40cdc-132">Namnet på den uttryckliga vägen i resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="40cdc-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="40cdc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40cdc-133">CommonParameters</span></span>
<span data-ttu-id="40cdc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40cdc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40cdc-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40cdc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40cdc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40cdc-136">INPUTS</span></span>

### <span data-ttu-id="40cdc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="40cdc-137">System.String</span></span>

## <span data-ttu-id="40cdc-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40cdc-138">OUTPUTS</span></span>

### <span data-ttu-id="40cdc-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40cdc-139">System.Boolean</span></span>

## <span data-ttu-id="40cdc-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40cdc-140">NOTES</span></span>

## <span data-ttu-id="40cdc-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40cdc-141">RELATED LINKS</span></span>