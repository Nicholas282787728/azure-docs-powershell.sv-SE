---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258839"
---
# <span data-ttu-id="9de53-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="9de53-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="9de53-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9de53-102">SYNOPSIS</span></span>
<span data-ttu-id="9de53-103">Hämta tillgängliga tjänst delegeringar i regionen.</span><span class="sxs-lookup"><span data-stu-id="9de53-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="9de53-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9de53-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9de53-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9de53-105">DESCRIPTION</span></span>
<span data-ttu-id="9de53-106">Med cmdleten **Get-AzAvailableServiceDelegation** kan du hämta alla tillgängliga tjänst delegeringar för ett undernät på den plats som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="9de53-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="9de53-107">Denna cmdlet beskriver *inte* vilka delegeringar som kan finnas tillsammans i ett enda undernät.</span><span class="sxs-lookup"><span data-stu-id="9de53-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="9de53-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9de53-108">EXAMPLES</span></span>

### <span data-ttu-id="9de53-109">1: få alla tillgängliga tjänst delegeringar</span><span class="sxs-lookup"><span data-stu-id="9de53-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="9de53-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9de53-110">PARAMETERS</span></span>

### <span data-ttu-id="9de53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de53-111">-DefaultProfile</span></span>
<span data-ttu-id="9de53-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9de53-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de53-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="9de53-113">-Location</span></span>
<span data-ttu-id="9de53-114">Platsen.</span><span class="sxs-lookup"><span data-stu-id="9de53-114">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de53-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de53-115">CommonParameters</span></span>
<span data-ttu-id="9de53-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de53-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de53-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9de53-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de53-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9de53-118">INPUTS</span></span>

### <span data-ttu-id="9de53-119">System. String</span><span class="sxs-lookup"><span data-stu-id="9de53-119">System.String</span></span>

## <span data-ttu-id="9de53-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9de53-120">OUTPUTS</span></span>

### <span data-ttu-id="9de53-121">Microsoft. Azure. commands. Networks. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="9de53-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="9de53-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9de53-122">NOTES</span></span>

## <span data-ttu-id="9de53-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9de53-123">RELATED LINKS</span></span>

<span data-ttu-id="9de53-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="9de53-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>