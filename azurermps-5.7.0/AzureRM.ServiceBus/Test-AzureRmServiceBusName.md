---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575494"
---
# <span data-ttu-id="76b0e-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="76b0e-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="76b0e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="76b0e-103">Kontrollerar tillgänglighet för det angivna namn området eller aliaset (DR-konfigurationsfilen)</span><span class="sxs-lookup"><span data-stu-id="76b0e-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76b0e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76b0e-104">SYNTAX</span></span>

### <span data-ttu-id="76b0e-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="76b0e-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76b0e-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="76b0e-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76b0e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76b0e-107">DESCRIPTION</span></span>
<span data-ttu-id="76b0e-108">**Test-AzureRmServiceBusName** cmdlet kontrollerar tillgänglighet för namn områdes namnet eller aliaset (Dr-konfigurationsfilen)</span><span class="sxs-lookup"><span data-stu-id="76b0e-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="76b0e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76b0e-109">EXAMPLES</span></span>

### <span data-ttu-id="76b0e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="76b0e-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="76b0e-111">Returnerar statusen för tillgänglighet för namn områdes namnet "MyNameSapceName" som sant</span><span class="sxs-lookup"><span data-stu-id="76b0e-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="76b0e-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="76b0e-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="76b0e-113">Returnerar status för tillgänglighet för namn områdes namnet "MyNameSapceName" som falskt med anledning</span><span class="sxs-lookup"><span data-stu-id="76b0e-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="76b0e-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="76b0e-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## <span data-ttu-id="76b0e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76b0e-115">PARAMETERS</span></span>

### <span data-ttu-id="76b0e-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="76b0e-116">-AliasName</span></span>
<span data-ttu-id="76b0e-117">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="76b0e-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b0e-118">-DefaultProfile</span></span>
<span data-ttu-id="76b0e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76b0e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b0e-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="76b0e-120">-Namespace</span></span>
<span data-ttu-id="76b0e-121">Namn namn för ServiceBus</span><span class="sxs-lookup"><span data-stu-id="76b0e-121">Servicebus Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b0e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b0e-122">-ResourceGroupName</span></span>
<span data-ttu-id="76b0e-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="76b0e-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76b0e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b0e-124">CommonParameters</span></span>
<span data-ttu-id="76b0e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76b0e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="76b0e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76b0e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b0e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76b0e-127">INPUTS</span></span>

### <span data-ttu-id="76b0e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="76b0e-128">System.String</span></span>


## <span data-ttu-id="76b0e-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76b0e-129">OUTPUTS</span></span>

### <span data-ttu-id="76b0e-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="76b0e-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="76b0e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76b0e-131">NOTES</span></span>

## <span data-ttu-id="76b0e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76b0e-132">RELATED LINKS</span></span>
