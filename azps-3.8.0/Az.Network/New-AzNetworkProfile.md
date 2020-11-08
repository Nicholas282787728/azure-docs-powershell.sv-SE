---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkProfile.md
ms.openlocfilehash: e463e6a1d25db24553b62c8d2fea1051eb231840
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089788"
---
# <span data-ttu-id="d6979-101">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d6979-101">New-AzNetworkProfile</span></span>

## <span data-ttu-id="d6979-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6979-102">SYNOPSIS</span></span>
<span data-ttu-id="d6979-103">Skapar en ny nätverks profil.</span><span class="sxs-lookup"><span data-stu-id="d6979-103">Creates a new network profile.</span></span>

## <span data-ttu-id="d6979-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6979-104">SYNTAX</span></span>

```
New-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Location <String>] [-Tag <Hashtable>]
 [-ContainerNicConfig <PSContainerNetworkInterfaceConfiguration[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6979-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6979-105">DESCRIPTION</span></span>
<span data-ttu-id="d6979-106">Cmdleten **New-AzNetworkProfile** skapar en ny nätverks profil på toppnivå resursen.</span><span class="sxs-lookup"><span data-stu-id="d6979-106">The **New-AzNetworkProfile** cmdlet creates a new network profile top level resource.</span></span>

## <span data-ttu-id="d6979-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6979-107">EXAMPLES</span></span>

### <span data-ttu-id="d6979-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d6979-108">Example 1</span></span>
```powershell
$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus
```

<span data-ttu-id="d6979-109">Då skapas en ny nätverks profil på toppnivå resursen</span><span class="sxs-lookup"><span data-stu-id="d6979-109">This creates a new network profile top level resource</span></span>

## <span data-ttu-id="d6979-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6979-110">PARAMETERS</span></span>

### <span data-ttu-id="d6979-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6979-111">-AsJob</span></span>
<span data-ttu-id="d6979-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d6979-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6979-113">-ContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d6979-113">-ContainerNicConfig</span></span>
<span data-ttu-id="d6979-114">Konfiguration av behållare för nätverks gränssnitt att lägga till i den här nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="d6979-114">The container network interface configurations to add to this network profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]
Parameter Sets: (All)
Aliases: ContainerNetworkInterfaceConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6979-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6979-115">-DefaultProfile</span></span>
<span data-ttu-id="d6979-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6979-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6979-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d6979-117">-Force</span></span>
<span data-ttu-id="d6979-118">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="d6979-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d6979-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="d6979-119">-Location</span></span>
<span data-ttu-id="d6979-120">Platsen.</span><span class="sxs-lookup"><span data-stu-id="d6979-120">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6979-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6979-121">-Name</span></span>
<span data-ttu-id="d6979-122">Namnet på nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="d6979-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6979-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6979-123">-ResourceGroupName</span></span>
<span data-ttu-id="d6979-124">Namnet på resurs gruppen för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="d6979-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6979-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d6979-125">-Tag</span></span>
<span data-ttu-id="d6979-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="d6979-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6979-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6979-127">-Confirm</span></span>
<span data-ttu-id="d6979-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6979-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6979-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6979-129">-WhatIf</span></span>
<span data-ttu-id="d6979-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6979-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6979-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6979-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6979-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6979-132">CommonParameters</span></span>
<span data-ttu-id="d6979-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6979-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6979-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6979-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6979-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6979-135">INPUTS</span></span>

### <span data-ttu-id="d6979-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d6979-136">System.String</span></span>

### <span data-ttu-id="d6979-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="d6979-137">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d6979-138">Microsoft. Azure. commands. Network. Models. PSContainerNetworkInterfaceConfiguration []</span><span class="sxs-lookup"><span data-stu-id="d6979-138">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration[]</span></span>

## <span data-ttu-id="d6979-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6979-139">OUTPUTS</span></span>

### <span data-ttu-id="d6979-140">Microsoft. Azure. commands. Networks. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d6979-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="d6979-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6979-141">NOTES</span></span>

## <span data-ttu-id="d6979-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6979-142">RELATED LINKS</span></span>

[<span data-ttu-id="d6979-143">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d6979-143">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="d6979-144">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d6979-144">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="d6979-145">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="d6979-145">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
