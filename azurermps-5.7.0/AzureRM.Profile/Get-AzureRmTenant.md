---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermtenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmTenant.md
ms.openlocfilehash: 7d9687877e3a27d175719a7a7b9ec6c78a529e52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581056"
---
# <span data-ttu-id="ebb10-101">Get-AzureRmTenant</span><span class="sxs-lookup"><span data-stu-id="ebb10-101">Get-AzureRmTenant</span></span>

## <span data-ttu-id="ebb10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ebb10-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb10-103">Får klient organisationer som har behörighet för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="ebb10-103">Gets tenants that are authorized for the current user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebb10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ebb10-104">SYNTAX</span></span>

```
Get-AzureRmTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebb10-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ebb10-105">DESCRIPTION</span></span>
<span data-ttu-id="ebb10-106">Get-AzureRmTenant-cmdleten får innehavare som är auktoriserade för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="ebb10-106">The Get-AzureRmTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="ebb10-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ebb10-107">EXAMPLES</span></span>

### <span data-ttu-id="ebb10-108">Exempel 1: Hämta alla innehavare</span><span class="sxs-lookup"><span data-stu-id="ebb10-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com

TenantId : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Domain   : microsoft.com
```

<span data-ttu-id="ebb10-109">Det här exemplet visar hur du får alla auktoriserade klient organisationer för ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="ebb10-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="ebb10-110">Exempel 2: skaffa en speciell klient organisation</span><span class="sxs-lookup"><span data-stu-id="ebb10-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

TenantId : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Domain   : microsoft.com
```

<span data-ttu-id="ebb10-111">Det här exemplet visar hur du får en viss auktoriserad klient organisation för ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="ebb10-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="ebb10-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ebb10-112">PARAMETERS</span></span>

### <span data-ttu-id="ebb10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb10-113">-DefaultProfile</span></span>
<span data-ttu-id="ebb10-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ebb10-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebb10-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ebb10-115">-TenantId</span></span>
<span data-ttu-id="ebb10-116">Anger ID för den klient organisation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="ebb10-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ebb10-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb10-117">CommonParameters</span></span>
<span data-ttu-id="ebb10-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebb10-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb10-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb10-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb10-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ebb10-120">INPUTS</span></span>

### <span data-ttu-id="ebb10-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="ebb10-121">None</span></span>
<span data-ttu-id="ebb10-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ebb10-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ebb10-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ebb10-123">OUTPUTS</span></span>

### <span data-ttu-id="ebb10-124">PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="ebb10-124">PSAzureTenant</span></span>
<span data-ttu-id="ebb10-125">Denna cmdlet returnerar klient-ID och associerad domän information för klient organisationer som har behörighet för det aktuella kontot.</span><span class="sxs-lookup"><span data-stu-id="ebb10-125">This cmdlet returns the tenant ID and associated domain information for tenants authorized for the current account.</span></span>

## <span data-ttu-id="ebb10-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ebb10-126">NOTES</span></span>

## <span data-ttu-id="ebb10-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ebb10-127">RELATED LINKS</span></span>

