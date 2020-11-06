---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: c22bb41702bb4e338d0548be6c7544d597ef0230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580803"
---
# <span data-ttu-id="397e3-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="397e3-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="397e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="397e3-102">SYNOPSIS</span></span>
<span data-ttu-id="397e3-103">Hämtar primär nyckelinformation för de angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="397e3-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="397e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="397e3-104">SYNTAX</span></span>

### <span data-ttu-id="397e3-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="397e3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="397e3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="397e3-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="397e3-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="397e3-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="397e3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="397e3-108">DESCRIPTION</span></span>
<span data-ttu-id="397e3-109">Den Get-AzureRmEventHubKey cmdleten returnerar primära och sekundära ConnectionString och nycklar Detaljer för angivna namn områdes-/händelse nav/aliasuppsättningar.</span><span class="sxs-lookup"><span data-stu-id="397e3-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="397e3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="397e3-110">EXAMPLES</span></span>

### <span data-ttu-id="397e3-111">Exempel 1 – namnrymd</span><span class="sxs-lookup"><span data-stu-id="397e3-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="397e3-112">Exempel 2 – EventHub</span><span class="sxs-lookup"><span data-stu-id="397e3-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="397e3-113">Hämtar information om primära och sekundära ConnectionString och nycklar för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="397e3-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="397e3-114">Exempel 3-alias (konfiguration för återställnings läge)</span><span class="sxs-lookup"><span data-stu-id="397e3-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="397e3-115">Hämtar information om primära, sekundära, AliasPrimary och AliasSecondary-ConnectionString och nycklar för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="397e3-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="397e3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="397e3-116">PARAMETERS</span></span>

### <span data-ttu-id="397e3-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="397e3-117">-AliasName</span></span>
<span data-ttu-id="397e3-118">Aliasnamn</span><span class="sxs-lookup"><span data-stu-id="397e3-118">Alias Name</span></span>

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

### <span data-ttu-id="397e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="397e3-119">-DefaultProfile</span></span>
<span data-ttu-id="397e3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="397e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="397e3-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="397e3-121">-EventHub</span></span>
<span data-ttu-id="397e3-122">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="397e3-122">EventHub Name</span></span>

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

### <span data-ttu-id="397e3-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="397e3-123">-Name</span></span>
<span data-ttu-id="397e3-124">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="397e3-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="397e3-125">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="397e3-125">-Namespace</span></span>
<span data-ttu-id="397e3-126">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="397e3-126">Namespace Name</span></span>

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

### <span data-ttu-id="397e3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="397e3-127">-ResourceGroupName</span></span>
<span data-ttu-id="397e3-128">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="397e3-128">Resource Group Name</span></span>

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

### <span data-ttu-id="397e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397e3-129">CommonParameters</span></span>
<span data-ttu-id="397e3-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="397e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397e3-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="397e3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397e3-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="397e3-132">INPUTS</span></span>

### <span data-ttu-id="397e3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="397e3-133">System.String</span></span>

## <span data-ttu-id="397e3-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="397e3-134">OUTPUTS</span></span>

### <span data-ttu-id="397e3-135">Microsoft. Azure. commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="397e3-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="397e3-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="397e3-136">NOTES</span></span>

## <span data-ttu-id="397e3-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="397e3-137">RELATED LINKS</span></span>
