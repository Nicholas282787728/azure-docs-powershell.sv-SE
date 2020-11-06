---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571751"
---
# <span data-ttu-id="967ad-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="967ad-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="967ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="967ad-102">SYNOPSIS</span></span>
<span data-ttu-id="967ad-103">Hämtar de metadata som används för att autentisera Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="967ad-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="967ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="967ad-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="967ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="967ad-105">DESCRIPTION</span></span>
<span data-ttu-id="967ad-106">Den Get-AzureRmContext cmdleten hämtar de aktuella metadata som används för att autentisera Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="967ad-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="967ad-107">Denna cmdlet hämtar Active Directory-kontot, Active Directory-klienten, Azure-prenumerationen och mål Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="967ad-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="967ad-108">Azure Resource Manager-cmdlets använder de här inställningarna som standard när du gör Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="967ad-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="967ad-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="967ad-109">EXAMPLES</span></span>

### <span data-ttu-id="967ad-110">Exempel 1: hämta den aktuella kontexten</span><span class="sxs-lookup"><span data-stu-id="967ad-110">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="967ad-111">I det här exemplet loggar vi in på vårt konto med ett Azure-abonnemang med hjälp av Add-AzureRmAccount och sedan hämtas den aktuella sessionens kontext genom att ringa get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="967ad-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="967ad-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="967ad-112">PARAMETERS</span></span>

### <span data-ttu-id="967ad-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="967ad-113">CommonParameters</span></span>
<span data-ttu-id="967ad-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="967ad-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="967ad-115">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="967ad-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="967ad-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="967ad-116">INPUTS</span></span>

## <span data-ttu-id="967ad-117">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="967ad-117">OUTPUTS</span></span>

### <span data-ttu-id="967ad-118">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="967ad-118">PSAzureContext</span></span>
<span data-ttu-id="967ad-119">Denna cmdlet returnerar det konto, den klient organisation och det abonnemang som används av Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="967ad-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="967ad-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="967ad-120">NOTES</span></span>

## <span data-ttu-id="967ad-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="967ad-121">RELATED LINKS</span></span>

[<span data-ttu-id="967ad-122">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="967ad-122">Set-AzureRMContext</span></span>]()

