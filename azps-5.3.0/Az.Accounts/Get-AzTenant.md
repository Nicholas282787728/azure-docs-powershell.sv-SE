---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-aztenant
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzTenant.md
ms.openlocfilehash: 936eb5bb7f49c2530a325b3bfa8c369b8f097711
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523364"
---
# <span data-ttu-id="ab97e-101">Get-AzTenant</span><span class="sxs-lookup"><span data-stu-id="ab97e-101">Get-AzTenant</span></span>

## <span data-ttu-id="ab97e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab97e-102">SYNOPSIS</span></span>
<span data-ttu-id="ab97e-103">Får klient organisationer som har behörighet för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="ab97e-103">Gets tenants that are authorized for the current user.</span></span>

## <span data-ttu-id="ab97e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab97e-104">SYNTAX</span></span>

```
Get-AzTenant [[-TenantId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab97e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab97e-105">DESCRIPTION</span></span>
<span data-ttu-id="ab97e-106">Get-AzTenant-cmdleten får innehavare som är auktoriserade för den aktuella användaren.</span><span class="sxs-lookup"><span data-stu-id="ab97e-106">The Get-AzTenant cmdlet gets tenants authorized for the current user.</span></span>

## <span data-ttu-id="ab97e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab97e-107">EXAMPLES</span></span>

### <span data-ttu-id="ab97e-108">Exempel 1: Hämta alla innehavare</span><span class="sxs-lookup"><span data-stu-id="ab97e-108">Example 1: Getting all tenants</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy Testhost    Home     testhost.onmicrosoft.com
```

<span data-ttu-id="ab97e-109">Det här exemplet visar hur du får alla auktoriserade klient organisationer för ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="ab97e-109">This example shows how to get all of the authorized tenants of an Azure account.</span></span>

### <span data-ttu-id="ab97e-110">Exempel 2: skaffa en speciell klient organisation</span><span class="sxs-lookup"><span data-stu-id="ab97e-110">Example 2: Getting a specific tenant</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzTenant -TenantId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

Id                                   Name        Category Domains
--                                   ----------- -------- -------
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft   Home     {test0.com, test1.com, test2.microsoft.com, test3.microsoft.com...}
```

<span data-ttu-id="ab97e-111">Det här exemplet visar hur du får en viss auktoriserad klient organisation för ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="ab97e-111">This example shows how to get a specific authorized tenant of an Azure account.</span></span>

## <span data-ttu-id="ab97e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab97e-112">PARAMETERS</span></span>

### <span data-ttu-id="ab97e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab97e-113">-DefaultProfile</span></span>
<span data-ttu-id="ab97e-114">Autentiseringsuppgifter, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ab97e-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab97e-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ab97e-115">-TenantId</span></span>
<span data-ttu-id="ab97e-116">Anger ID för den klient organisation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="ab97e-116">Specifies the ID of the tenant that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain, Tenant

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab97e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab97e-117">CommonParameters</span></span>
<span data-ttu-id="ab97e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab97e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab97e-119">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab97e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab97e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab97e-120">INPUTS</span></span>

### <span data-ttu-id="ab97e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ab97e-121">System.String</span></span>

## <span data-ttu-id="ab97e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab97e-122">OUTPUTS</span></span>

### <span data-ttu-id="ab97e-123">Microsoft. Azure. commands. Profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="ab97e-123">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

## <span data-ttu-id="ab97e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab97e-124">NOTES</span></span>

## <span data-ttu-id="ab97e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab97e-125">RELATED LINKS</span></span>
