---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubRegistryStatistic.md
ms.openlocfilehash: 033a7be2da102274837c881337fcb8f5bca4b879
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756595"
---
# <span data-ttu-id="c6634-101">Get-AzureRmIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="c6634-101">Get-AzureRmIotHubRegistryStatistic</span></span>

## <span data-ttu-id="c6634-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6634-102">SYNOPSIS</span></span>
<span data-ttu-id="c6634-103">Hämtar RegistryStatistics för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="c6634-103">Gets the RegistryStatistics for an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6634-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6634-104">SYNTAX</span></span>

```
Get-AzureRmIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6634-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6634-105">DESCRIPTION</span></span>
<span data-ttu-id="c6634-106">Hämtar RegistryStatistics för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="c6634-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="c6634-107">Här finns information om antalet enheter med total summa, aktiverade och inaktiverade i en IotHub.</span><span class="sxs-lookup"><span data-stu-id="c6634-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="c6634-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6634-108">EXAMPLES</span></span>

### <span data-ttu-id="c6634-109">Exempel 1 skaffa RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="c6634-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzureRmIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c6634-110">Hämtar RegistryStatictics för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c6634-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c6634-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6634-111">PARAMETERS</span></span>

### <span data-ttu-id="c6634-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6634-112">-Name</span></span>
<span data-ttu-id="c6634-113">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="c6634-113">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6634-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6634-114">-ResourceGroupName</span></span>
<span data-ttu-id="c6634-115">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c6634-115">Resource Group Name</span></span>

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

### <span data-ttu-id="c6634-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6634-116">-DefaultProfile</span></span>
<span data-ttu-id="c6634-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6634-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6634-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6634-118">CommonParameters</span></span>
<span data-ttu-id="c6634-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6634-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6634-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6634-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6634-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6634-121">INPUTS</span></span>

### <span data-ttu-id="c6634-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c6634-122">System.String</span></span>

## <span data-ttu-id="c6634-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6634-123">OUTPUTS</span></span>

### <span data-ttu-id="c6634-124">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubRegistryStatistics, Microsoft. Azure. commands. IotHub, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c6634-124">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c6634-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6634-125">NOTES</span></span>

## <span data-ttu-id="c6634-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6634-126">RELATED LINKS</span></span>

