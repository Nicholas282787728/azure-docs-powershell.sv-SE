---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 143604052fbbec594af0093ee94cbbadafac14d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754077"
---
# <span data-ttu-id="5f55e-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="5f55e-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="5f55e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f55e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f55e-103">Hämtar primär nyckelinformation för de angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="5f55e-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="5f55e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f55e-104">SYNTAX</span></span>

### <span data-ttu-id="5f55e-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5f55e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f55e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5f55e-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f55e-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="5f55e-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f55e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f55e-108">DESCRIPTION</span></span>
<span data-ttu-id="5f55e-109">Den Get-AzEventHubKey cmdleten returnerar primära och sekundära ConnectionString och nycklar Detaljer för angivna namn områdes-/händelse nav/aliasuppsättningar.</span><span class="sxs-lookup"><span data-stu-id="5f55e-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="5f55e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f55e-110">EXAMPLES</span></span>

### <span data-ttu-id="5f55e-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="5f55e-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="5f55e-112">Exempel 2 – EventHub</span><span class="sxs-lookup"><span data-stu-id="5f55e-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="5f55e-113">Hämtar information om primära och sekundära ConnectionString och nycklar för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="5f55e-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="5f55e-114">Exempel 3-alias (konfiguration för återställnings läge)</span><span class="sxs-lookup"><span data-stu-id="5f55e-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="5f55e-115">Hämtar information om primära, sekundära, AliasPrimary och AliasSecondary-ConnectionString och nycklar för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="5f55e-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="5f55e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f55e-116">PARAMETERS</span></span>

### <span data-ttu-id="5f55e-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="5f55e-117">-AliasName</span></span>
<span data-ttu-id="5f55e-118">Aliasnamn</span><span class="sxs-lookup"><span data-stu-id="5f55e-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f55e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f55e-119">-DefaultProfile</span></span>
<span data-ttu-id="5f55e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f55e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f55e-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5f55e-121">-EventHub</span></span>
<span data-ttu-id="5f55e-122">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="5f55e-122">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f55e-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f55e-123">-Name</span></span>
<span data-ttu-id="5f55e-124">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="5f55e-124">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f55e-125">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="5f55e-125">-Namespace</span></span>
<span data-ttu-id="5f55e-126">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="5f55e-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f55e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f55e-127">-ResourceGroupName</span></span>
<span data-ttu-id="5f55e-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5f55e-128">Resource Group Name</span></span>

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

### <span data-ttu-id="5f55e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f55e-129">CommonParameters</span></span>
<span data-ttu-id="5f55e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f55e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f55e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f55e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f55e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f55e-132">INPUTS</span></span>

### <span data-ttu-id="5f55e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5f55e-133">System.String</span></span>

## <span data-ttu-id="5f55e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f55e-134">OUTPUTS</span></span>

### <span data-ttu-id="5f55e-135">Microsoft. Azure. commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="5f55e-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="5f55e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f55e-136">NOTES</span></span>

## <span data-ttu-id="5f55e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f55e-137">RELATED LINKS</span></span>