---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322167"
---
# <span data-ttu-id="5f804-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="5f804-101">Test-AzRelayName</span></span>

## <span data-ttu-id="5f804-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f804-102">SYNOPSIS</span></span>
<span data-ttu-id="5f804-103">Kontrollerar tillgänglighet för det angivna namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="5f804-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="5f804-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f804-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f804-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f804-105">DESCRIPTION</span></span>
<span data-ttu-id="5f804-106">**Test-AzRelayName** cmdlet kontrollerar tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="5f804-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="5f804-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f804-107">EXAMPLES</span></span>

### <span data-ttu-id="5f804-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5f804-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="5f804-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5f804-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="5f804-110">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="5f804-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="5f804-111">Returnerar statusen för tillgänglighet för namn områdes namnet</span><span class="sxs-lookup"><span data-stu-id="5f804-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="5f804-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f804-112">PARAMETERS</span></span>

### <span data-ttu-id="5f804-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f804-113">-DefaultProfile</span></span>
<span data-ttu-id="5f804-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f804-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f804-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="5f804-115">-Namespace</span></span>
<span data-ttu-id="5f804-116">Namn på relä området.</span><span class="sxs-lookup"><span data-stu-id="5f804-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="5f804-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f804-117">CommonParameters</span></span>
<span data-ttu-id="5f804-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f804-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f804-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f804-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f804-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f804-120">INPUTS</span></span>

### <span data-ttu-id="5f804-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5f804-121">System.String</span></span>

## <span data-ttu-id="5f804-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f804-122">OUTPUTS</span></span>

### <span data-ttu-id="5f804-123">Microsoft. Azure. commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="5f804-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="5f804-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f804-124">NOTES</span></span>

## <span data-ttu-id="5f804-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f804-125">RELATED LINKS</span></span>
