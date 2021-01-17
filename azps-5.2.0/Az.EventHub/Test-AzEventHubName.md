---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401339"
---
# <span data-ttu-id="9b06e-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="9b06e-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="9b06e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b06e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b06e-103">Kontrollerar tillgänglighet för det angivna namn området eller aliaset (DR-konfigurationsfilen)</span><span class="sxs-lookup"><span data-stu-id="9b06e-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="9b06e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b06e-104">SYNTAX</span></span>

### <span data-ttu-id="9b06e-105">NamespaceCheckNameAvailabilitySet (standard)</span><span class="sxs-lookup"><span data-stu-id="9b06e-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b06e-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9b06e-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b06e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b06e-107">DESCRIPTION</span></span>
<span data-ttu-id="9b06e-108">**Test-AzEventhubName** cmdlet kontrollerar tillgänglighet för namn områdes namnet eller aliaset (Dr-konfigurationsfilen)</span><span class="sxs-lookup"><span data-stu-id="9b06e-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="9b06e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b06e-109">EXAMPLES</span></span>

### <span data-ttu-id="9b06e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b06e-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="9b06e-111">Returnerar statusen för tillgänglighet för namn områdes namnet "MyNameSapceName" som sant om tillgängligt</span><span class="sxs-lookup"><span data-stu-id="9b06e-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="9b06e-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9b06e-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="9b06e-113">Returnerar status för tillgänglighet för namn områdes namnet "MyNameSapceName" som falskt med anledning</span><span class="sxs-lookup"><span data-stu-id="9b06e-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="9b06e-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9b06e-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="9b06e-115">Returnerar statusen för tillgänglighet för aliasnamnet ' myAliasName ' för namn området ' MyNameSapceName ' som sant om tillgängligt</span><span class="sxs-lookup"><span data-stu-id="9b06e-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="9b06e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b06e-116">PARAMETERS</span></span>

### <span data-ttu-id="9b06e-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="9b06e-117">-AliasName</span></span>
<span data-ttu-id="9b06e-118">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="9b06e-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b06e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b06e-119">-DefaultProfile</span></span>
<span data-ttu-id="9b06e-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b06e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b06e-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9b06e-121">-Namespace</span></span>
<span data-ttu-id="9b06e-122">Namn område för Eventhub</span><span class="sxs-lookup"><span data-stu-id="9b06e-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="9b06e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b06e-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b06e-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9b06e-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b06e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b06e-125">CommonParameters</span></span>
<span data-ttu-id="9b06e-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b06e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b06e-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b06e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b06e-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b06e-128">INPUTS</span></span>

### <span data-ttu-id="9b06e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9b06e-129">System.String</span></span>

## <span data-ttu-id="9b06e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b06e-130">OUTPUTS</span></span>

### <span data-ttu-id="9b06e-131">Microsoft. Azure. commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="9b06e-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="9b06e-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b06e-132">NOTES</span></span>

## <span data-ttu-id="9b06e-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b06e-133">RELATED LINKS</span></span>
