---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: dbe93ca98fe8cf7a0a22f2b52a17a17e7222c261
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574779"
---
# <span data-ttu-id="fd9b2-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="fd9b2-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="fd9b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd9b2-103">Hämtar de metadata som används för att autentisera Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd9b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd9b2-104">SYNTAX</span></span>

### <span data-ttu-id="fd9b2-105">GetSingleContext (standard)</span><span class="sxs-lookup"><span data-stu-id="fd9b2-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="fd9b2-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="fd9b2-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd9b2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd9b2-107">DESCRIPTION</span></span>
<span data-ttu-id="fd9b2-108">Den Get-AzureRmContext cmdleten hämtar de aktuella metadata som används för att autentisera Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="fd9b2-109">Denna cmdlet hämtar Active Directory-kontot, Active Directory-klienten, Azure-prenumerationen och mål Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="fd9b2-110">Azure Resource Manager-cmdlets använder de här inställningarna som standard när du gör Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="fd9b2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd9b2-111">EXAMPLES</span></span>

### <span data-ttu-id="fd9b2-112">Exempel 1: hämta den aktuella kontexten</span><span class="sxs-lookup"><span data-stu-id="fd9b2-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="fd9b2-113">I det här exemplet loggar vi in på vårt konto med ett Azure-abonnemang med Connect-AzureRmAccount och sedan får du kontexten för den aktuella sessionen genom att ringa get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="fd9b2-114">Exempel 2: Visa alla tillgängliga kontexter</span><span class="sxs-lookup"><span data-stu-id="fd9b2-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="fd9b2-115">I det här exemplet visas alla tillgängliga kontexter.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="fd9b2-116">Användaren kan välja en av dessa sammanhang med Select-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="fd9b2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd9b2-117">PARAMETERS</span></span>

### <span data-ttu-id="fd9b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd9b2-118">-DefaultProfile</span></span>
<span data-ttu-id="fd9b2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fd9b2-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9b2-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="fd9b2-120">-ListAvailable</span></span>
<span data-ttu-id="fd9b2-121">Visa alla tillgängliga kontexter i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9b2-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="fd9b2-122">-Name</span></span>
<span data-ttu-id="fd9b2-123">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="fd9b2-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd9b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd9b2-124">CommonParameters</span></span>
<span data-ttu-id="fd9b2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd9b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd9b2-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd9b2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd9b2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd9b2-127">INPUTS</span></span>

### <span data-ttu-id="fd9b2-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="fd9b2-128">None</span></span>

## <span data-ttu-id="fd9b2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd9b2-129">OUTPUTS</span></span>

### <span data-ttu-id="fd9b2-130">Microsoft. Azure. commands. Profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="fd9b2-130">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="fd9b2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd9b2-131">NOTES</span></span>

## <span data-ttu-id="fd9b2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd9b2-132">RELATED LINKS</span></span>

[<span data-ttu-id="fd9b2-133">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="fd9b2-133">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

