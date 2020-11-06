---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2cabb88c490c7fdea56fd5ffde280cfd55bc8f3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571744"
---
# <span data-ttu-id="b5679-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="b5679-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="b5679-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5679-102">SYNOPSIS</span></span>
<span data-ttu-id="b5679-103">Får klient organisationer som har behörighet för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="b5679-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="b5679-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5679-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="b5679-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5679-105">DESCRIPTION</span></span>
<span data-ttu-id="b5679-106">Get-AzureRmTenant-cmdleten får innehavare som är auktoriserade för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="b5679-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="b5679-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5679-107">EXAMPLES</span></span>

### <span data-ttu-id="b5679-108">Exempel 1: Hämta alla innehavare</span><span class="sxs-lookup"><span data-stu-id="b5679-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="b5679-109">Det här exemplet visar hur du får alla auktoriserade klient organisationer för ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="b5679-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="b5679-110">Exempel 2: skaffa en speciell klient organisation</span><span class="sxs-lookup"><span data-stu-id="b5679-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="b5679-111">Det här exemplet visar hur du får en viss auktoriserad klient organisation för ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="b5679-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="b5679-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5679-112">PARAMETERS</span></span>

### <span data-ttu-id="b5679-113">-TenantId</span><span class="sxs-lookup"><span data-stu-id="b5679-113">-TenantId</span></span>
<span data-ttu-id="b5679-114">Anger ID för den klient organisation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="b5679-114">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5679-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5679-115">CommonParameters</span></span>
<span data-ttu-id="b5679-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5679-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5679-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5679-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5679-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5679-118">INPUTS</span></span>

## <span data-ttu-id="b5679-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5679-119">OUTPUTS</span></span>

### <span data-ttu-id="b5679-120">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="b5679-120">PSAzureTenant</span></span>
<span data-ttu-id="b5679-121">Denna cmdlet returnerar klient-ID och associerad domän information för klient organisationer som har behörighet för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="b5679-121">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="b5679-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5679-122">NOTES</span></span>

## <span data-ttu-id="b5679-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5679-123">RELATED LINKS</span></span>

