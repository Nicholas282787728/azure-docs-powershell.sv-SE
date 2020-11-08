---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94093060"
---
# <span data-ttu-id="ef022-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="ef022-101">Get-AzsOffer</span></span>

## <span data-ttu-id="ef022-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef022-102">SYNOPSIS</span></span>
<span data-ttu-id="ef022-103">Hämta listan med offentliga erbjudanden till rot leverantören.</span><span class="sxs-lookup"><span data-stu-id="ef022-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="ef022-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef022-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ef022-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef022-105">DESCRIPTION</span></span>
<span data-ttu-id="ef022-106">Hämta listan med offentliga erbjudanden till rot leverantören.</span><span class="sxs-lookup"><span data-stu-id="ef022-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="ef022-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef022-107">EXAMPLES</span></span>

### <span data-ttu-id="ef022-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef022-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="ef022-109">Hämta listan med offentliga erbjudanden</span><span class="sxs-lookup"><span data-stu-id="ef022-109">Get the list of public offers</span></span>

## <span data-ttu-id="ef022-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef022-110">PARAMETERS</span></span>

### <span data-ttu-id="ef022-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef022-111">-DefaultProfile</span></span>
<span data-ttu-id="ef022-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef022-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef022-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef022-113">CommonParameters</span></span>
<span data-ttu-id="ef022-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef022-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef022-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef022-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef022-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef022-116">INPUTS</span></span>

## <span data-ttu-id="ef022-117">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef022-117">OUTPUTS</span></span>

### <span data-ttu-id="ef022-118">Microsoft. Azure. PowerShell. cmdletar. Subscription. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="ef022-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="ef022-119">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef022-119">NOTES</span></span>

## <span data-ttu-id="ef022-120">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef022-120">RELATED LINKS</span></span>

