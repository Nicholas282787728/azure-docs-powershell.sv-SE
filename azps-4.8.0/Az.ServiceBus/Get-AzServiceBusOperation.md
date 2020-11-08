---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100851"
---
# <span data-ttu-id="fb7a4-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="fb7a4-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="fb7a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb7a4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7a4-103">Lista över ServiceBus-åtgärder som stöds</span><span class="sxs-lookup"><span data-stu-id="fb7a4-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="fb7a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb7a4-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb7a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb7a4-105">DESCRIPTION</span></span>
<span data-ttu-id="fb7a4-106">Cmdleten **Get-AzServiceBusOperation** innehåller en lista med de ServiceBus-funktioner som stöds.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="fb7a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb7a4-107">EXAMPLES</span></span>

### <span data-ttu-id="fb7a4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fb7a4-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="fb7a4-109">Här listas ServiceBus-funktioner som stöds</span><span class="sxs-lookup"><span data-stu-id="fb7a4-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="fb7a4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb7a4-110">PARAMETERS</span></span>

### <span data-ttu-id="fb7a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7a4-111">-DefaultProfile</span></span>
<span data-ttu-id="fb7a4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb7a4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7a4-113">CommonParameters</span></span>
<span data-ttu-id="fb7a4-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb7a4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7a4-115">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb7a4-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7a4-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb7a4-116">INPUTS</span></span>

### <span data-ttu-id="fb7a4-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="fb7a4-117">None</span></span>

## <span data-ttu-id="fb7a4-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb7a4-118">OUTPUTS</span></span>

### <span data-ttu-id="fb7a4-119">Microsoft. Azure. commands. ServiceBus. Models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="fb7a4-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="fb7a4-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb7a4-120">NOTES</span></span>

## <span data-ttu-id="fb7a4-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb7a4-121">RELATED LINKS</span></span>