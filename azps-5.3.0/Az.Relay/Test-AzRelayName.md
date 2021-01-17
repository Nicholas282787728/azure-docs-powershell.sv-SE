---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421072"
---
# <span data-ttu-id="59428-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="59428-101">Test-AzRelayName</span></span>

## <span data-ttu-id="59428-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59428-102">SYNOPSIS</span></span>
<span data-ttu-id="59428-103">Kontrollerar tillgänglighet för det angivna namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="59428-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="59428-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59428-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59428-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59428-105">DESCRIPTION</span></span>
<span data-ttu-id="59428-106">**Test-AzRelayName** cmdlet kontrollerar tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="59428-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="59428-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59428-107">EXAMPLES</span></span>

### <span data-ttu-id="59428-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59428-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="59428-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="59428-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="59428-110">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="59428-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="59428-111">Returnerar statusen för tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="59428-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="59428-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59428-112">PARAMETERS</span></span>

### <span data-ttu-id="59428-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59428-113">-DefaultProfile</span></span>
<span data-ttu-id="59428-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59428-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59428-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="59428-115">-Namespace</span></span>
<span data-ttu-id="59428-116">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="59428-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="59428-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59428-117">CommonParameters</span></span>
<span data-ttu-id="59428-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59428-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59428-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59428-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59428-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59428-120">INPUTS</span></span>

### <span data-ttu-id="59428-121">System. String</span><span class="sxs-lookup"><span data-stu-id="59428-121">System.String</span></span>

## <span data-ttu-id="59428-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59428-122">OUTPUTS</span></span>

### <span data-ttu-id="59428-123">Microsoft. Azure. commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="59428-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="59428-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59428-124">NOTES</span></span>

## <span data-ttu-id="59428-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59428-125">RELATED LINKS</span></span>
