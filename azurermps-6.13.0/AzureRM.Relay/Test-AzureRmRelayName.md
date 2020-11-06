---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 396243e366f6a21e2ac94d105473b348c6a8198d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581664"
---
# <span data-ttu-id="70bfd-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="70bfd-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="70bfd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70bfd-102">SYNOPSIS</span></span>
<span data-ttu-id="70bfd-103">Kontrollerar tillgänglighet för det angivna namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="70bfd-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70bfd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70bfd-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70bfd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70bfd-105">DESCRIPTION</span></span>
<span data-ttu-id="70bfd-106">**Test-AzureRmRelayName** cmdlet kontrollerar tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="70bfd-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="70bfd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70bfd-107">EXAMPLES</span></span>

### <span data-ttu-id="70bfd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="70bfd-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="70bfd-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="70bfd-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="70bfd-110">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="70bfd-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="70bfd-111">Returnerar statusen för tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="70bfd-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="70bfd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70bfd-112">PARAMETERS</span></span>

### <span data-ttu-id="70bfd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bfd-113">-DefaultProfile</span></span>
<span data-ttu-id="70bfd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70bfd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70bfd-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="70bfd-115">-Namespace</span></span>
<span data-ttu-id="70bfd-116">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="70bfd-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="70bfd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bfd-117">CommonParameters</span></span>
<span data-ttu-id="70bfd-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70bfd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="70bfd-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bfd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bfd-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70bfd-120">INPUTS</span></span>

### <span data-ttu-id="70bfd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="70bfd-121">System.String</span></span>


## <span data-ttu-id="70bfd-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70bfd-122">OUTPUTS</span></span>

### <span data-ttu-id="70bfd-123">Microsoft. Azure. commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="70bfd-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="70bfd-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70bfd-124">NOTES</span></span>

## <span data-ttu-id="70bfd-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70bfd-125">RELATED LINKS</span></span>
