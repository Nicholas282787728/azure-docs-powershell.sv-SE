---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527659"
---
# <span data-ttu-id="27dd4-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="27dd4-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="27dd4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="27dd4-103">Tar bort en befintlig P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="27dd4-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="27dd4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27dd4-104">SYNTAX</span></span>

### <span data-ttu-id="27dd4-105">ByP2SVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="27dd4-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dd4-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="27dd4-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27dd4-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="27dd4-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27dd4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27dd4-108">DESCRIPTION</span></span>
<span data-ttu-id="27dd4-109">Med cmdleten **Remove-AzP2sVpnGateway** kan du ta bort en befintlig P2SVpnGateway under VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="27dd4-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="27dd4-110">Alla anslutningar till klient klienter Miss lyckas när P2SVpnGateway har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="27dd4-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="27dd4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27dd4-111">EXAMPLES</span></span>

### <span data-ttu-id="27dd4-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="27dd4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="27dd4-113">Med cmdleten **Remove-AzP2sVpnGateway** kan du ta bort en befintlig P2SVpnGateway under VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="27dd4-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="27dd4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27dd4-114">PARAMETERS</span></span>

### <span data-ttu-id="27dd4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27dd4-115">-DefaultProfile</span></span>
<span data-ttu-id="27dd4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27dd4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27dd4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="27dd4-117">-Force</span></span>
<span data-ttu-id="27dd4-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="27dd4-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="27dd4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27dd4-119">-InputObject</span></span>
<span data-ttu-id="27dd4-120">P2sVpnGateway-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="27dd4-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27dd4-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="27dd4-121">-Name</span></span>
<span data-ttu-id="27dd4-122">P2SVpnGateway namn.</span><span class="sxs-lookup"><span data-stu-id="27dd4-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27dd4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27dd4-123">-PassThru</span></span>
<span data-ttu-id="27dd4-124">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="27dd4-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="27dd4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27dd4-125">-ResourceGroupName</span></span>
<span data-ttu-id="27dd4-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="27dd4-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27dd4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27dd4-127">-ResourceId</span></span>
<span data-ttu-id="27dd4-128">Azure Resource ID för p2sVpnGateway ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="27dd4-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27dd4-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27dd4-129">-Confirm</span></span>
<span data-ttu-id="27dd4-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27dd4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27dd4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27dd4-131">-WhatIf</span></span>
<span data-ttu-id="27dd4-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27dd4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27dd4-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="27dd4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27dd4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27dd4-134">CommonParameters</span></span>
<span data-ttu-id="27dd4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27dd4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27dd4-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27dd4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27dd4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27dd4-137">INPUTS</span></span>

### <span data-ttu-id="27dd4-138">Microsoft. Azure. commands. Networks. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="27dd4-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="27dd4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27dd4-139">System.String</span></span>

## <span data-ttu-id="27dd4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27dd4-140">OUTPUTS</span></span>

### <span data-ttu-id="27dd4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27dd4-141">System.Boolean</span></span>

## <span data-ttu-id="27dd4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27dd4-142">NOTES</span></span>

## <span data-ttu-id="27dd4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27dd4-143">RELATED LINKS</span></span>
