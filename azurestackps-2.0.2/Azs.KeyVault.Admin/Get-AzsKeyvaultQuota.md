---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100332"
---
# <span data-ttu-id="39cea-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="39cea-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="39cea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39cea-102">SYNOPSIS</span></span>
<span data-ttu-id="39cea-103">Få en lista över alla kvot objekt för ett valv på en plats.</span><span class="sxs-lookup"><span data-stu-id="39cea-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="39cea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39cea-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="39cea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39cea-105">DESCRIPTION</span></span>
<span data-ttu-id="39cea-106">Få en lista över alla kvot objekt för ett valv på en plats.</span><span class="sxs-lookup"><span data-stu-id="39cea-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="39cea-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39cea-107">EXAMPLES</span></span>

### <span data-ttu-id="39cea-108">Exempel 1:</span><span class="sxs-lookup"><span data-stu-id="39cea-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="39cea-109">Få en lista över alla kvot objekt för ett valv på en plats.</span><span class="sxs-lookup"><span data-stu-id="39cea-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="39cea-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39cea-110">PARAMETERS</span></span>

### <span data-ttu-id="39cea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39cea-111">-DefaultProfile</span></span>
<span data-ttu-id="39cea-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39cea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39cea-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="39cea-113">-Location</span></span>
<span data-ttu-id="39cea-114">Plats för kvoten.</span><span class="sxs-lookup"><span data-stu-id="39cea-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39cea-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39cea-115">-SubscriptionId</span></span>
<span data-ttu-id="39cea-116">Autentiseringsuppgifter för prenumerationer som unikt identifierar Microsoft Azure-prenumerationen. Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="39cea-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="39cea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39cea-117">CommonParameters</span></span>
<span data-ttu-id="39cea-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39cea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39cea-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39cea-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39cea-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39cea-120">INPUTS</span></span>

## <span data-ttu-id="39cea-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39cea-121">OUTPUTS</span></span>

### <span data-ttu-id="39cea-122">Microsoft. Azure. PowerShell. cmdletar. KeyVaultAdmin. Models. Api20170201Preview. IQuota</span><span class="sxs-lookup"><span data-stu-id="39cea-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="39cea-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39cea-123">NOTES</span></span>

## <span data-ttu-id="39cea-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39cea-124">RELATED LINKS</span></span>
