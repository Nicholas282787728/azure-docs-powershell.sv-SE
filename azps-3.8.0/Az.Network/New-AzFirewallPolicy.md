---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925590"
---
# <span data-ttu-id="9cb88-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="9cb88-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="9cb88-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cb88-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb88-103">Skapar en ny Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="9cb88-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="9cb88-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cb88-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb88-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cb88-105">DESCRIPTION</span></span>
<span data-ttu-id="9cb88-106">Cmdleten **New-AzFirewallPolicy** skapar en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="9cb88-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="9cb88-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cb88-107">EXAMPLES</span></span>

### <span data-ttu-id="9cb88-108">1. skapa en tom princip</span><span class="sxs-lookup"><span data-stu-id="9cb88-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="9cb88-109">I det här exemplet skapas en Azure Firewall-princip</span><span class="sxs-lookup"><span data-stu-id="9cb88-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="9cb88-110">2. skapa en tom princip med ThreatIntel-läge</span><span class="sxs-lookup"><span data-stu-id="9cb88-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="9cb88-111">I det här exemplet skapas en Azure Firewall-princip med ett hot Intel-läge</span><span class="sxs-lookup"><span data-stu-id="9cb88-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="9cb88-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cb88-112">PARAMETERS</span></span>

### <span data-ttu-id="9cb88-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cb88-113">-AsJob</span></span>
<span data-ttu-id="9cb88-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9cb88-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cb88-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="9cb88-115">-BasePolicy</span></span>
<span data-ttu-id="9cb88-116">Åtgärds läget för Threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="9cb88-116">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="9cb88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb88-117">-DefaultProfile</span></span>
<span data-ttu-id="9cb88-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb88-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb88-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9cb88-119">-Force</span></span>
<span data-ttu-id="9cb88-120">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="9cb88-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9cb88-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="9cb88-121">-Location</span></span>
<span data-ttu-id="9cb88-122">plats.</span><span class="sxs-lookup"><span data-stu-id="9cb88-122">location.</span></span>

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

### <span data-ttu-id="9cb88-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="9cb88-123">-Name</span></span>
<span data-ttu-id="9cb88-124">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="9cb88-124">The resource name.</span></span>

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

### <span data-ttu-id="9cb88-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb88-125">-ResourceGroupName</span></span>
<span data-ttu-id="9cb88-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9cb88-126">The resource group name.</span></span>

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

### <span data-ttu-id="9cb88-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9cb88-127">-Tag</span></span>
<span data-ttu-id="9cb88-128">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="9cb88-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9cb88-129">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="9cb88-129">-ThreatIntelMode</span></span>
<span data-ttu-id="9cb88-130">Åtgärds läget för Threat intelligence.</span><span class="sxs-lookup"><span data-stu-id="9cb88-130">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cb88-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9cb88-131">-Confirm</span></span>
<span data-ttu-id="9cb88-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cb88-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb88-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb88-133">-WhatIf</span></span>
<span data-ttu-id="9cb88-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9cb88-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb88-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9cb88-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb88-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb88-136">CommonParameters</span></span>
<span data-ttu-id="9cb88-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb88-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb88-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9cb88-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb88-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cb88-139">INPUTS</span></span>

### <span data-ttu-id="9cb88-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9cb88-140">System.String</span></span>

### <span data-ttu-id="9cb88-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="9cb88-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9cb88-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cb88-142">OUTPUTS</span></span>

### <span data-ttu-id="9cb88-143">Microsoft. Azure. commands. Networks. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="9cb88-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="9cb88-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cb88-144">NOTES</span></span>

## <span data-ttu-id="9cb88-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cb88-145">RELATED LINKS</span></span>
