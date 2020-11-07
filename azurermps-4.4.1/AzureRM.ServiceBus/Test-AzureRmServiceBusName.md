---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757455"
---
# <span data-ttu-id="f9a35-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="f9a35-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="f9a35-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9a35-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a35-103">Kontrollerar tillgänglighet för det angivna namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="f9a35-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a35-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9a35-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="f9a35-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9a35-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a35-106">**Test-AzureRmServiceBusName** cmdlet kontrollerar tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="f9a35-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="f9a35-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9a35-107">EXAMPLES</span></span>

### <span data-ttu-id="f9a35-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f9a35-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="f9a35-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f9a35-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="f9a35-110">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="f9a35-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="f9a35-111">Returnerar statusen för tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="f9a35-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="f9a35-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9a35-112">PARAMETERS</span></span>

### <span data-ttu-id="f9a35-113">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f9a35-113">-Namespace</span></span>
<span data-ttu-id="f9a35-114">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="f9a35-114">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="f9a35-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a35-115">CommonParameters</span></span>
<span data-ttu-id="f9a35-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a35-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a35-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a35-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a35-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9a35-118">INPUTS</span></span>

### <span data-ttu-id="f9a35-119">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f9a35-119">-Namespace</span></span>
 <span data-ttu-id="f9a35-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f9a35-120">System.String</span></span>

## <span data-ttu-id="f9a35-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9a35-121">OUTPUTS</span></span>

### <span data-ttu-id="f9a35-122">[Microsoft. Azure. kommandon. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. commands. ServiceBus, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="f9a35-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="f9a35-123">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f9a35-123">Example 1</span></span>
<span data-ttu-id="f9a35-124">NameAvailable skäl</span><span class="sxs-lookup"><span data-stu-id="f9a35-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="f9a35-125">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f9a35-125">Example 2</span></span>
<span data-ttu-id="f9a35-126">NameAvailable skäl</span><span class="sxs-lookup"><span data-stu-id="f9a35-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="f9a35-127">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="f9a35-127">Example 3</span></span>
<span data-ttu-id="f9a35-128">NameAvailable skäl</span><span class="sxs-lookup"><span data-stu-id="f9a35-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="f9a35-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9a35-129">NOTES</span></span>

## <span data-ttu-id="f9a35-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9a35-130">RELATED LINKS</span></span>
