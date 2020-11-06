---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 96b9b5a6bec10082d7b004dcede73b743a7e538b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583116"
---
# <span data-ttu-id="b4fdb-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="b4fdb-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="b4fdb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4fdb-102">SYNOPSIS</span></span>
<span data-ttu-id="b4fdb-103">Hämtar de metadata som används för att autentisera Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4fdb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4fdb-104">SYNTAX</span></span>

### <span data-ttu-id="b4fdb-105">GetSingleContext (standard)</span><span class="sxs-lookup"><span data-stu-id="b4fdb-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4fdb-106">ListAllContexts</span><span class="sxs-lookup"><span data-stu-id="b4fdb-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4fdb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4fdb-107">DESCRIPTION</span></span>
<span data-ttu-id="b4fdb-108">Den Get-AzureRmContext cmdleten hämtar de aktuella metadata som används för att autentisera Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="b4fdb-109">Denna cmdlet hämtar Active Directory-kontot, Active Directory-klienten, Azure-prenumerationen och mål Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="b4fdb-110">Azure Resource Manager-cmdlets använder de här inställningarna som standard när du gör Azure Resource Manager-begäranden.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="b4fdb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4fdb-111">EXAMPLES</span></span>

### <span data-ttu-id="b4fdb-112">Exempel 1: hämta den aktuella kontexten</span><span class="sxs-lookup"><span data-stu-id="b4fdb-112">Example 1: Getting the current context</span></span>
```
PS C:\> Connect-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="b4fdb-113">I det här exemplet loggar vi in på vårt konto med ett Azure-abonnemang med Connect-AzureRmAccount och sedan får du kontexten för den aktuella sessionen genom att ringa get-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-113">In this example we are logging into our account with an Azure subscription using Connect-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="b4fdb-114">Exempel 2: Visa alla tillgängliga kontexter</span><span class="sxs-lookup"><span data-stu-id="b4fdb-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

<span data-ttu-id="b4fdb-115">I det här exemplet visas alla tillgängliga kontexter.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="b4fdb-116">Användaren kan välja en av dessa sammanhang med Select-AzureRmContext.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="b4fdb-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4fdb-117">PARAMETERS</span></span>

### <span data-ttu-id="b4fdb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4fdb-118">-DefaultProfile</span></span>
<span data-ttu-id="b4fdb-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b4fdb-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4fdb-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="b4fdb-120">-ListAvailable</span></span>
<span data-ttu-id="b4fdb-121">Visa alla tillgängliga kontexter i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-121">List all available contexts in the current session.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fdb-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4fdb-122">-Name</span></span>
<span data-ttu-id="b4fdb-123">Kontextens namn</span><span class="sxs-lookup"><span data-stu-id="b4fdb-123">The name of the context</span></span>

```yaml
Type: String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: Default

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4fdb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4fdb-124">CommonParameters</span></span>
<span data-ttu-id="b4fdb-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4fdb-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4fdb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4fdb-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4fdb-127">INPUTS</span></span>

### <span data-ttu-id="b4fdb-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="b4fdb-128">None</span></span>
<span data-ttu-id="b4fdb-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b4fdb-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4fdb-130">OUTPUTS</span></span>

### <span data-ttu-id="b4fdb-131">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="b4fdb-131">PSAzureContext</span></span>
<span data-ttu-id="b4fdb-132">Denna cmdlet returnerar det konto, den klient organisation och det abonnemang som används av Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="b4fdb-132">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="b4fdb-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4fdb-133">NOTES</span></span>

## <span data-ttu-id="b4fdb-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4fdb-134">RELATED LINKS</span></span>

[<span data-ttu-id="b4fdb-135">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="b4fdb-135">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

