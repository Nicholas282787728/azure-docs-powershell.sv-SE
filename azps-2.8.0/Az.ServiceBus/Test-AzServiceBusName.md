---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: 0c094fbc294ac6ca5370f8d82c8ebfceac74af0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919946"
---
# <span data-ttu-id="c48ad-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="c48ad-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="c48ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c48ad-102">SYNOPSIS</span></span>
<span data-ttu-id="c48ad-103">Kontrollerar tillgänglighet för det angivna namn området eller aliaset (DR-konfigurationsfilen)</span><span class="sxs-lookup"><span data-stu-id="c48ad-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="c48ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c48ad-104">SYNTAX</span></span>

### <span data-ttu-id="c48ad-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c48ad-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c48ad-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c48ad-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c48ad-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c48ad-107">DESCRIPTION</span></span>
<span data-ttu-id="c48ad-108">**Test-AzServiceBusName** cmdlet kontrollerar tillgänglighet för namn områdes namnet eller aliaset (Dr-konfigurationsfilen)</span><span class="sxs-lookup"><span data-stu-id="c48ad-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="c48ad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c48ad-109">EXAMPLES</span></span>

### <span data-ttu-id="c48ad-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c48ad-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="c48ad-111">Returnerar statusen för tillgänglighet för namn områdes namnet "MyNameSapceName" som sant</span><span class="sxs-lookup"><span data-stu-id="c48ad-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="c48ad-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c48ad-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="c48ad-113">Returnerar status för tillgänglighet för namn områdes namnet "MyNameSapceName" som falskt med anledning</span><span class="sxs-lookup"><span data-stu-id="c48ad-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="c48ad-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="c48ad-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="c48ad-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c48ad-115">PARAMETERS</span></span>

### <span data-ttu-id="c48ad-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="c48ad-116">-AliasName</span></span>
<span data-ttu-id="c48ad-117">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="c48ad-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="c48ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48ad-118">-DefaultProfile</span></span>
<span data-ttu-id="c48ad-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c48ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c48ad-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c48ad-120">-Namespace</span></span>
<span data-ttu-id="c48ad-121">Namn namn för ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c48ad-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48ad-122">-ResourceGroupName</span></span>
<span data-ttu-id="c48ad-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c48ad-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48ad-124">CommonParameters</span></span>
<span data-ttu-id="c48ad-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48ad-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c48ad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48ad-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c48ad-127">INPUTS</span></span>

### <span data-ttu-id="c48ad-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c48ad-128">System.String</span></span>

## <span data-ttu-id="c48ad-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c48ad-129">OUTPUTS</span></span>

### <span data-ttu-id="c48ad-130">Microsoft. Azure. commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="c48ad-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="c48ad-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c48ad-131">NOTES</span></span>

## <span data-ttu-id="c48ad-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c48ad-132">RELATED LINKS</span></span>