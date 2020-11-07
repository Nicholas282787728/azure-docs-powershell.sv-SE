---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747786"
---
# <span data-ttu-id="e3a87-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e3a87-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="e3a87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3a87-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a87-103">Uppdaterar en brand Väggs princip för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e3a87-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="e3a87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3a87-104">SYNTAX</span></span>

### <span data-ttu-id="e3a87-105">ByFactoryObject (standard)</span><span class="sxs-lookup"><span data-stu-id="e3a87-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3a87-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="e3a87-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3a87-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e3a87-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3a87-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3a87-108">DESCRIPTION</span></span>
<span data-ttu-id="e3a87-109">Cmdleten **set-AzApplicationGatewayFirewallPolicy** uppdaterar en Azure Application Gateway-brandvägg.</span><span class="sxs-lookup"><span data-stu-id="e3a87-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="e3a87-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3a87-110">EXAMPLES</span></span>

### <span data-ttu-id="e3a87-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e3a87-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="e3a87-112">Det här kommandot uppdaterar brand Väggs principen för Application Gateway med inställningarna i $AppGwFirewallPolicy variabel och lagrar den uppdaterade gatewayen i $UpdatedAppGwFirewallPolicy-variabeln.</span><span class="sxs-lookup"><span data-stu-id="e3a87-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="e3a87-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3a87-113">PARAMETERS</span></span>

### <span data-ttu-id="e3a87-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3a87-114">-AsJob</span></span>
<span data-ttu-id="e3a87-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e3a87-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3a87-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="e3a87-116">-CustomRule</span></span>
<span data-ttu-id="e3a87-117">Listan med CustomRules</span><span class="sxs-lookup"><span data-stu-id="e3a87-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a87-118">-DefaultProfile</span></span>
<span data-ttu-id="e3a87-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a87-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3a87-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3a87-120">-InputObject</span></span>
<span data-ttu-id="e3a87-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e3a87-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3a87-122">-Name</span></span>
<span data-ttu-id="e3a87-123">Namnet på brand Väggs principen.</span><span class="sxs-lookup"><span data-stu-id="e3a87-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a87-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3a87-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e3a87-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3a87-126">-ResourceId</span></span>
<span data-ttu-id="e3a87-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="e3a87-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a87-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a87-128">CommonParameters</span></span>
<span data-ttu-id="e3a87-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a87-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a87-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a87-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a87-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3a87-131">INPUTS</span></span>

### <span data-ttu-id="e3a87-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e3a87-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="e3a87-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3a87-133">OUTPUTS</span></span>

### <span data-ttu-id="e3a87-134">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e3a87-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="e3a87-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3a87-135">NOTES</span></span>

## <span data-ttu-id="e3a87-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3a87-136">RELATED LINKS</span></span>
