---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 547069954ada24531e1551b75c4065416eeae1fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918778"
---
# <span data-ttu-id="c0cf0-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="c0cf0-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="c0cf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cf0-103">Hämta tillgängliga tjänst delegeringar i regionen.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="c0cf0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0cf0-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0cf0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0cf0-105">DESCRIPTION</span></span>
<span data-ttu-id="c0cf0-106">Med cmdleten **Get-AzAvailableServiceDelegation** kan du hämta alla tillgängliga tjänst delegeringar för ett undernät på den plats som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="c0cf0-107">Denna cmdlet beskriver *inte* vilka delegeringar som kan finnas tillsammans i ett enda undernät.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="c0cf0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0cf0-108">EXAMPLES</span></span>

### <span data-ttu-id="c0cf0-109">1: få alla tillgängliga tjänst delegeringar</span><span class="sxs-lookup"><span data-stu-id="c0cf0-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="c0cf0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0cf0-110">PARAMETERS</span></span>

### <span data-ttu-id="c0cf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cf0-111">-DefaultProfile</span></span>
<span data-ttu-id="c0cf0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0cf0-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="c0cf0-113">-Location</span></span>
<span data-ttu-id="c0cf0-114">Platsen.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-114">The location.</span></span>

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

### <span data-ttu-id="c0cf0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cf0-115">CommonParameters</span></span>
<span data-ttu-id="c0cf0-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0cf0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cf0-117">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0cf0-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cf0-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0cf0-118">INPUTS</span></span>

### <span data-ttu-id="c0cf0-119">System. String</span><span class="sxs-lookup"><span data-stu-id="c0cf0-119">System.String</span></span>

## <span data-ttu-id="c0cf0-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0cf0-120">OUTPUTS</span></span>

### <span data-ttu-id="c0cf0-121">Microsoft. Azure. commands. Networks. Models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="c0cf0-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="c0cf0-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0cf0-122">NOTES</span></span>

## <span data-ttu-id="c0cf0-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0cf0-123">RELATED LINKS</span></span>

<span data-ttu-id="c0cf0-124">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="c0cf0-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>