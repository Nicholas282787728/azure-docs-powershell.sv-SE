---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: bb4ab11406a644d34bdb5b45ea3b3fba47376826
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916457"
---
# <span data-ttu-id="bacdb-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="bacdb-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="bacdb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bacdb-102">SYNOPSIS</span></span>
<span data-ttu-id="bacdb-103">Hämtar RegistryStatistics för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="bacdb-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="bacdb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bacdb-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bacdb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bacdb-105">DESCRIPTION</span></span>
<span data-ttu-id="bacdb-106">Hämtar RegistryStatistics för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="bacdb-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="bacdb-107">Här finns information om antalet enheter med total summa, aktiverade och inaktiverade i en IotHub.</span><span class="sxs-lookup"><span data-stu-id="bacdb-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="bacdb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bacdb-108">EXAMPLES</span></span>

### <span data-ttu-id="bacdb-109">Exempel 1 skaffa RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="bacdb-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="bacdb-110">Hämtar RegistryStatictics för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="bacdb-110">Gets the RegistryStatictics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="bacdb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bacdb-111">PARAMETERS</span></span>

### <span data-ttu-id="bacdb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bacdb-112">-DefaultProfile</span></span>
<span data-ttu-id="bacdb-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bacdb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bacdb-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="bacdb-114">-Name</span></span>
<span data-ttu-id="bacdb-115">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="bacdb-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="bacdb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bacdb-116">-ResourceGroupName</span></span>
<span data-ttu-id="bacdb-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bacdb-117">Resource Group Name</span></span>

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

### <span data-ttu-id="bacdb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bacdb-118">CommonParameters</span></span>
<span data-ttu-id="bacdb-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bacdb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bacdb-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bacdb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bacdb-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bacdb-121">INPUTS</span></span>

### <span data-ttu-id="bacdb-122">System. String</span><span class="sxs-lookup"><span data-stu-id="bacdb-122">System.String</span></span>

## <span data-ttu-id="bacdb-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bacdb-123">OUTPUTS</span></span>

### <span data-ttu-id="bacdb-124">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="bacdb-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="bacdb-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bacdb-125">NOTES</span></span>

## <span data-ttu-id="bacdb-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bacdb-126">RELATED LINKS</span></span>
