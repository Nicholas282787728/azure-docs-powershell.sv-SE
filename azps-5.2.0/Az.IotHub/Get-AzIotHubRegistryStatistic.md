---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubregistrystatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRegistryStatistic.md
ms.openlocfilehash: 36d59745b19df716735ce5b9b248c0ca71b7d687
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417131"
---
# <span data-ttu-id="d8b4c-101">Get-AzIotHubRegistryStatistic</span><span class="sxs-lookup"><span data-stu-id="d8b4c-101">Get-AzIotHubRegistryStatistic</span></span>

## <span data-ttu-id="d8b4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b4c-103">Hämtar RegistryStatistics för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="d8b4c-103">Gets the RegistryStatistics for an IotHub.</span></span>

## <span data-ttu-id="d8b4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8b4c-104">SYNTAX</span></span>

```
Get-AzIotHubRegistryStatistic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8b4c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8b4c-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b4c-106">Hämtar RegistryStatistics för en IotHub.</span><span class="sxs-lookup"><span data-stu-id="d8b4c-106">Gets the RegistryStatistics for an IotHub.</span></span>
<span data-ttu-id="d8b4c-107">Här finns information om antalet enheter med total summa, aktiverade och inaktiverade i en IotHub.</span><span class="sxs-lookup"><span data-stu-id="d8b4c-107">This provides information about the number of total, enabled and disabled devices in an IotHub.</span></span>

## <span data-ttu-id="d8b4c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8b4c-108">EXAMPLES</span></span>

### <span data-ttu-id="d8b4c-109">Exempel 1 skaffa RegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="d8b4c-109">Example 1 Get the RegistryStatistics</span></span>
```
PS C:\> Get-AzIotHubRegistryStatistic -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d8b4c-110">Hämtar RegistryStatistics för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d8b4c-110">Gets the RegistryStatistics for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d8b4c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8b4c-111">PARAMETERS</span></span>

### <span data-ttu-id="d8b4c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b4c-112">-DefaultProfile</span></span>
<span data-ttu-id="d8b4c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d8b4c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8b4c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8b4c-114">-Name</span></span>
<span data-ttu-id="d8b4c-115">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="d8b4c-115">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="d8b4c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b4c-116">-ResourceGroupName</span></span>
<span data-ttu-id="d8b4c-117">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d8b4c-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d8b4c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b4c-118">CommonParameters</span></span>
<span data-ttu-id="d8b4c-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b4c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b4c-120">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b4c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b4c-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8b4c-121">INPUTS</span></span>

### <span data-ttu-id="d8b4c-122">System. String</span><span class="sxs-lookup"><span data-stu-id="d8b4c-122">System.String</span></span>

## <span data-ttu-id="d8b4c-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8b4c-123">OUTPUTS</span></span>

### <span data-ttu-id="d8b4c-124">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubRegistryStatistics</span><span class="sxs-lookup"><span data-stu-id="d8b4c-124">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubRegistryStatistics</span></span>

## <span data-ttu-id="d8b4c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8b4c-125">NOTES</span></span>

## <span data-ttu-id="d8b4c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8b4c-126">RELATED LINKS</span></span>
