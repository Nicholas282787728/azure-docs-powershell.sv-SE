---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: e70ff7da7c005f6376d3c4e7a6aae5295e53f693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579992"
---
# <span data-ttu-id="34576-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="34576-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="34576-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34576-102">SYNOPSIS</span></span>
<span data-ttu-id="34576-103">Lista över ServiceBus-åtgärder som stöds</span><span class="sxs-lookup"><span data-stu-id="34576-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34576-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34576-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34576-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34576-105">DESCRIPTION</span></span>
<span data-ttu-id="34576-106">Cmdleten **Get-AzureRmServiceBusOperation** innehåller en lista med de ServiceBus-funktioner som stöds.</span><span class="sxs-lookup"><span data-stu-id="34576-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="34576-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34576-107">EXAMPLES</span></span>

### <span data-ttu-id="34576-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="34576-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="34576-109">Här listas ServiceBus-funktioner som stöds</span><span class="sxs-lookup"><span data-stu-id="34576-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="34576-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34576-110">PARAMETERS</span></span>

### <span data-ttu-id="34576-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34576-111">-DefaultProfile</span></span>
<span data-ttu-id="34576-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34576-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34576-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34576-113">CommonParameters</span></span>
<span data-ttu-id="34576-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34576-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34576-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34576-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34576-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34576-116">INPUTS</span></span>

### <span data-ttu-id="34576-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="34576-117">None</span></span>

## <span data-ttu-id="34576-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34576-118">OUTPUTS</span></span>

### <span data-ttu-id="34576-119">Microsoft. Azure. commands. ServiceBus. Models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="34576-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="34576-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34576-120">NOTES</span></span>

## <span data-ttu-id="34576-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34576-121">RELATED LINKS</span></span>
