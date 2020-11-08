---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091664"
---
# <span data-ttu-id="ab624-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab624-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="ab624-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab624-102">SYNOPSIS</span></span>
<span data-ttu-id="ab624-103">Tar bort en befintlig VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ab624-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="ab624-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab624-104">SYNTAX</span></span>

### <span data-ttu-id="ab624-105">ByVpnServerConfigurationName (standard)</span><span class="sxs-lookup"><span data-stu-id="ab624-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab624-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="ab624-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab624-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="ab624-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab624-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab624-108">DESCRIPTION</span></span>
<span data-ttu-id="ab624-109">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="ab624-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ab624-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab624-110">EXAMPLES</span></span>

### <span data-ttu-id="ab624-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ab624-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="ab624-112">Kommandot ovan tar bort en befintlig VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ab624-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="ab624-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab624-113">PARAMETERS</span></span>

### <span data-ttu-id="ab624-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab624-114">-DefaultProfile</span></span>
<span data-ttu-id="ab624-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab624-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab624-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ab624-116">-Force</span></span>
<span data-ttu-id="ab624-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ab624-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ab624-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab624-118">-InputObject</span></span>
<span data-ttu-id="ab624-119">VpnServerConfiguration-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ab624-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab624-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab624-120">-Name</span></span>
<span data-ttu-id="ab624-121">VpnServerConfiguration namn.</span><span class="sxs-lookup"><span data-stu-id="ab624-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab624-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab624-122">-PassThru</span></span>
<span data-ttu-id="ab624-123">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="ab624-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="ab624-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab624-124">-ResourceGroupName</span></span>
<span data-ttu-id="ab624-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ab624-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab624-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab624-126">-ResourceId</span></span>
<span data-ttu-id="ab624-127">Azure Resource ID för vpnServerConfiguration ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ab624-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab624-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab624-128">-Confirm</span></span>
<span data-ttu-id="ab624-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab624-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab624-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab624-130">-WhatIf</span></span>
<span data-ttu-id="ab624-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab624-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab624-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab624-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab624-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab624-133">CommonParameters</span></span>
<span data-ttu-id="ab624-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab624-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab624-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab624-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab624-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab624-136">INPUTS</span></span>

### <span data-ttu-id="ab624-137">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab624-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="ab624-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ab624-138">System.String</span></span>

## <span data-ttu-id="ab624-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab624-139">OUTPUTS</span></span>

### <span data-ttu-id="ab624-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab624-140">System.Boolean</span></span>

## <span data-ttu-id="ab624-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab624-141">NOTES</span></span>

## <span data-ttu-id="ab624-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab624-142">RELATED LINKS</span></span>
