---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579451"
---
# <span data-ttu-id="72130-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="72130-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="72130-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72130-102">SYNOPSIS</span></span>
<span data-ttu-id="72130-103">Kontrollerar tillgänglighet för det angivna namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="72130-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72130-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72130-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72130-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72130-105">DESCRIPTION</span></span>
<span data-ttu-id="72130-106">**Test-AzureRmRelayName** cmdlet kontrollerar tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="72130-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="72130-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72130-107">EXAMPLES</span></span>

### <span data-ttu-id="72130-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="72130-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="72130-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="72130-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="72130-110">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="72130-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="72130-111">Returnerar statusen för tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="72130-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="72130-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72130-112">PARAMETERS</span></span>

### <span data-ttu-id="72130-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72130-113">-DefaultProfile</span></span>
<span data-ttu-id="72130-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72130-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72130-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="72130-115">-Namespace</span></span>
<span data-ttu-id="72130-116">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="72130-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="72130-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72130-117">CommonParameters</span></span>
<span data-ttu-id="72130-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72130-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72130-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72130-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72130-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72130-120">INPUTS</span></span>

### <span data-ttu-id="72130-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="72130-121">-Namespace</span></span>
 <span data-ttu-id="72130-122">System. String</span><span class="sxs-lookup"><span data-stu-id="72130-122">System.String</span></span>

## <span data-ttu-id="72130-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72130-123">OUTPUTS</span></span>

### <span data-ttu-id="72130-124">[Microsoft. Azure. commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. commands. Relay, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="72130-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="72130-125">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="72130-125">Example 1</span></span>
<span data-ttu-id="72130-126">NameAvailable skäl</span><span class="sxs-lookup"><span data-stu-id="72130-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="72130-127">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="72130-127">Example 2</span></span>
<span data-ttu-id="72130-128">NameAvailable skäl</span><span class="sxs-lookup"><span data-stu-id="72130-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="72130-129">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="72130-129">Example 3</span></span>
<span data-ttu-id="72130-130">NameAvailable skäl</span><span class="sxs-lookup"><span data-stu-id="72130-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="72130-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72130-131">NOTES</span></span>

## <span data-ttu-id="72130-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72130-132">RELATED LINKS</span></span>

