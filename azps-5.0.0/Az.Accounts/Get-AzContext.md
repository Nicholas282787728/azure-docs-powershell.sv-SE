---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContext.md
ms.openlocfilehash: dab6388205c00ee457b7f8095f0f529f591b304f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269530"
---
# <span data-ttu-id="4a447-101">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="4a447-101">Get-AzContext</span></span>

## <span data-ttu-id="4a447-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a447-102">SYNOPSIS</span></span>
<span data-ttu-id="4a447-103">Hämtar de metadata som används för att autentisera Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="4a447-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="4a447-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a447-104">SYNTAX</span></span>

### <span data-ttu-id="4a447-105">GetSingleContext (standard)</span><span class="sxs-lookup"><span data-stu-id="4a447-105">GetSingleContext (Default)</span></span>
```
Get-AzContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="4a447-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="4a447-106">ListAllContexts</span></span>
```
Get-AzContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a447-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a447-107">DESCRIPTION</span></span>
<span data-ttu-id="4a447-108">Den Get-AzContext cmdleten hämtar de aktuella metadata som används för att autentisera Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="4a447-108">The Get-AzContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>
<span data-ttu-id="4a447-109">Denna cmdlet hämtar Active Directory-kontot, Active Directory-klienten, Azure-prenumerationen och mål Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="4a447-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="4a447-110">Azure Resource Manager-cmdlets använder de här inställningarna som standard när du gör Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="4a447-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="4a447-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a447-111">EXAMPLES</span></span>

### <span data-ttu-id="4a447-112">Exempel 1: hämta den aktuella kontexten</span><span class="sxs-lookup"><span data-stu-id="4a447-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzAccount
PS C:\> Get-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="4a447-113">I det här exemplet loggar vi in på vårt konto med ett Azure-abonnemang med Connect-AzAccount och sedan får du kontexten för den aktuella sessionen genom att ringa get-AzContext.</span><span class="sxs-lookup"><span data-stu-id="4a447-113">In this example we are logging into our account with an Azure subscription using Connect-AzAccount, and then we are getting the context of the current session by calling Get-AzContext.</span></span>

### <span data-ttu-id="4a447-114">Exempel 2: Visa alla tillgängliga kontexter</span><span class="sxs-lookup"><span data-stu-id="4a447-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzContext -ListAvailable

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
Subscription2 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription2       AzureCloud          xxxxxxxx-x...
Subscription3 (xxxxxxxx-xxxx-xxxx-xxx... test@outlook.com    Subscription3       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="4a447-115">I det här exemplet visas alla tillgängliga kontexter.</span><span class="sxs-lookup"><span data-stu-id="4a447-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="4a447-116">Användaren kan välja en av dessa sammanhang med Select-AzContext.</span><span class="sxs-lookup"><span data-stu-id="4a447-116">The user may select one of these contexts using Select-AzContext.</span></span>

## <span data-ttu-id="4a447-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a447-117">PARAMETERS</span></span>

### <span data-ttu-id="4a447-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a447-118">-DefaultProfile</span></span>
<span data-ttu-id="4a447-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4a447-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a447-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="4a447-120">-ListAvailable</span></span>
<span data-ttu-id="4a447-121">Visa alla tillgängliga kontexter i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="4a447-121">List all available contexts in the current session.</span></span>

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

### <span data-ttu-id="4a447-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a447-122">-Name</span></span>
<span data-ttu-id="4a447-123">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="4a447-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a447-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a447-124">CommonParameters</span></span>
<span data-ttu-id="4a447-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a447-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a447-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a447-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a447-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a447-127">INPUTS</span></span>

### <span data-ttu-id="4a447-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="4a447-128">None</span></span>

## <span data-ttu-id="4a447-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a447-129">OUTPUTS</span></span>

### <span data-ttu-id="4a447-130">Microsoft. Azure. commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="4a447-130">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="4a447-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a447-131">NOTES</span></span>

## <span data-ttu-id="4a447-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a447-132">RELATED LINKS</span></span>

[<span data-ttu-id="4a447-133">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="4a447-133">Set-AzContext</span></span>](./Set-AzContext.md)

