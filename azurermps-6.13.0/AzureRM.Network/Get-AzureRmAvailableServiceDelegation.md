---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756674"
---
# <span data-ttu-id="79cb7-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="79cb7-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="79cb7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="79cb7-103">Hämta tillgängliga tjänst delegeringar i regionen.</span><span class="sxs-lookup"><span data-stu-id="79cb7-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79cb7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79cb7-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79cb7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79cb7-105">DESCRIPTION</span></span>
<span data-ttu-id="79cb7-106">Med cmdleten **Get-AzureRmAvailableServiceDelegation** kan du hämta alla tillgängliga tjänst delegeringar för ett undernät på den plats som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="79cb7-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="79cb7-107">Denna cmdlet beskriver *inte* vilka delegeringar som kan finnas tillsammans i ett enda undernät.</span><span class="sxs-lookup"><span data-stu-id="79cb7-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="79cb7-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79cb7-108">EXAMPLES</span></span>

### <span data-ttu-id="79cb7-109">1: få alla tillgängliga tjänst delegeringar</span><span class="sxs-lookup"><span data-stu-id="79cb7-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="79cb7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79cb7-110">PARAMETERS</span></span>

### <span data-ttu-id="79cb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79cb7-111">-DefaultProfile</span></span>
<span data-ttu-id="79cb7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79cb7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79cb7-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="79cb7-113">-Location</span></span>
<span data-ttu-id="79cb7-114">Platsen.</span><span class="sxs-lookup"><span data-stu-id="79cb7-114">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79cb7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79cb7-115">CommonParameters</span></span>
<span data-ttu-id="79cb7-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79cb7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="79cb7-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79cb7-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79cb7-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79cb7-118">INPUTS</span></span>

### <span data-ttu-id="79cb7-119">System. String</span><span class="sxs-lookup"><span data-stu-id="79cb7-119">System.String</span></span>

## <span data-ttu-id="79cb7-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79cb7-120">OUTPUTS</span></span>

### <span data-ttu-id="79cb7-121">Microsoft. Azure. commands. Networks. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="79cb7-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="79cb7-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79cb7-122">NOTES</span></span>

## <span data-ttu-id="79cb7-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79cb7-123">RELATED LINKS</span></span>
<span data-ttu-id="79cb7-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="79cb7-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>
