---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271325"
---
# <span data-ttu-id="36786-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="36786-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="36786-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36786-102">SYNOPSIS</span></span>
<span data-ttu-id="36786-103">Tar bort en befintlig VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="36786-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="36786-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36786-104">SYNTAX</span></span>

### <span data-ttu-id="36786-105">ByVpnServerConfigurationName (standard)</span><span class="sxs-lookup"><span data-stu-id="36786-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36786-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="36786-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36786-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="36786-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36786-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36786-108">DESCRIPTION</span></span>
<span data-ttu-id="36786-109">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="36786-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="36786-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36786-110">EXAMPLES</span></span>

### <span data-ttu-id="36786-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="36786-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="36786-112">Kommandot ovan tar bort en befintlig VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="36786-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="36786-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36786-113">PARAMETERS</span></span>

### <span data-ttu-id="36786-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36786-114">-DefaultProfile</span></span>
<span data-ttu-id="36786-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36786-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36786-116">-Force</span><span class="sxs-lookup"><span data-stu-id="36786-116">-Force</span></span>
<span data-ttu-id="36786-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="36786-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36786-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36786-118">-InputObject</span></span>
<span data-ttu-id="36786-119">VpnServerConfiguration-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="36786-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="36786-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="36786-120">-Name</span></span>
<span data-ttu-id="36786-121">VpnServerConfiguration namn.</span><span class="sxs-lookup"><span data-stu-id="36786-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="36786-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36786-122">-PassThru</span></span>
<span data-ttu-id="36786-123">Returnerar ett objekt som representerar objektet som den här åtgärden utförs på.</span><span class="sxs-lookup"><span data-stu-id="36786-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="36786-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36786-124">-ResourceGroupName</span></span>
<span data-ttu-id="36786-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="36786-125">The resource group name.</span></span>

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

### <span data-ttu-id="36786-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36786-126">-ResourceId</span></span>
<span data-ttu-id="36786-127">Azure Resource ID för vpnServerConfiguration ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="36786-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="36786-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="36786-128">-Confirm</span></span>
<span data-ttu-id="36786-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="36786-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36786-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36786-130">-WhatIf</span></span>
<span data-ttu-id="36786-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="36786-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36786-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="36786-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36786-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36786-133">CommonParameters</span></span>
<span data-ttu-id="36786-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36786-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36786-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36786-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36786-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36786-136">INPUTS</span></span>

### <span data-ttu-id="36786-137">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="36786-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="36786-138">System. String</span><span class="sxs-lookup"><span data-stu-id="36786-138">System.String</span></span>

## <span data-ttu-id="36786-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36786-139">OUTPUTS</span></span>

### <span data-ttu-id="36786-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36786-140">System.Boolean</span></span>

## <span data-ttu-id="36786-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36786-141">NOTES</span></span>

## <span data-ttu-id="36786-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36786-142">RELATED LINKS</span></span>
