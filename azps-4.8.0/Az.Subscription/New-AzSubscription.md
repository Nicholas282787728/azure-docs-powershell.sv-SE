---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
ms.openlocfilehash: 167678bfe84117cdc53e9e90b520abe24fed4b92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258972"
---
# <span data-ttu-id="2943f-101">New-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="2943f-101">New-AzSubscription</span></span>

## <span data-ttu-id="2943f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2943f-102">SYNOPSIS</span></span>
<span data-ttu-id="2943f-103">Skapar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="2943f-103">Creates an Azure subscription.</span></span>

## <span data-ttu-id="2943f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2943f-104">SYNTAX</span></span>

```
New-AzSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2943f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2943f-105">DESCRIPTION</span></span>
<span data-ttu-id="2943f-106">Cmdleten **New-AzSubscription** skapar en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="2943f-106">The **New-AzSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="2943f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2943f-107">EXAMPLES</span></span>

### <span data-ttu-id="2943f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2943f-108">Example 1</span></span>
```
PS C:\> New-AzSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="2943f-109">Skapar ett Azure-abonnemang under det angivna registrerings kontot med den angivna erbjudande typen.</span><span class="sxs-lookup"><span data-stu-id="2943f-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="2943f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2943f-110">PARAMETERS</span></span>

### <span data-ttu-id="2943f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2943f-111">-AsJob</span></span>
<span data-ttu-id="2943f-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2943f-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2943f-113">-DefaultProfile</span></span>
<span data-ttu-id="2943f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2943f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2943f-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="2943f-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="2943f-116">Namnet på det registrerings konto som ska användas när du skapar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2943f-116">Name of the enrollment account to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2943f-117">-Name</span></span>
<span data-ttu-id="2943f-118">Namnet på den prenumeration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2943f-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-119">-OfferType</span><span class="sxs-lookup"><span data-stu-id="2943f-119">-OfferType</span></span>
<span data-ttu-id="2943f-120">Den typ av erbjudande som ska användas när du skapar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2943f-120">The type of offer to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="2943f-121">-OwnerApplicationId</span></span>
<span data-ttu-id="2943f-122">Programmets SPN-namn för att få ägar åtkomst till prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2943f-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="2943f-123">-OwnerObjectId</span></span>
<span data-ttu-id="2943f-124">Användare eller grupp-ID: n som ska få ägar åtkomst till prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2943f-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="2943f-125">-OwnerSignInName</span></span>
<span data-ttu-id="2943f-126">Användaren/användarna som ska få ägar åtkomst till prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="2943f-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2943f-127">-Confirm</span></span>
<span data-ttu-id="2943f-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2943f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2943f-129">-WhatIf</span></span>
<span data-ttu-id="2943f-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2943f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2943f-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2943f-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2943f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2943f-132">CommonParameters</span></span>
<span data-ttu-id="2943f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2943f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2943f-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2943f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2943f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2943f-135">INPUTS</span></span>

### <span data-ttu-id="2943f-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="2943f-136">None</span></span>

## <span data-ttu-id="2943f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2943f-137">OUTPUTS</span></span>

### <span data-ttu-id="2943f-138">Microsoft. Azure. commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="2943f-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="2943f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2943f-139">NOTES</span></span>

## <span data-ttu-id="2943f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2943f-140">RELATED LINKS</span></span>