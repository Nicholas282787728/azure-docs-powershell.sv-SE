---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: 441681cd33fe7715fbbb6fb244848c287f14ebb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574639"
---
# <span data-ttu-id="3330c-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3330c-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="3330c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3330c-102">SYNOPSIS</span></span>
<span data-ttu-id="3330c-103">Hämtar integrerings konton.</span><span class="sxs-lookup"><span data-stu-id="3330c-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3330c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3330c-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3330c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3330c-105">DESCRIPTION</span></span>
<span data-ttu-id="3330c-106">Cmdleten **Get-AzureRmIntegrationAccount** hämtar integrerings konton från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3330c-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="3330c-107">Ange namnet på integrations kontot och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3330c-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="3330c-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="3330c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3330c-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="3330c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3330c-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="3330c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3330c-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="3330c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3330c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3330c-112">EXAMPLES</span></span>

### <span data-ttu-id="3330c-113">Exempel 1: skaffa ett integrations konto efter namn</span><span class="sxs-lookup"><span data-stu-id="3330c-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="3330c-114">Det här kommandot får ett integrerings konto med namnet IntegrationAccount31 från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3330c-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="3330c-115">Exempel 2: skaffa integrerings konton i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="3330c-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="3330c-116">Det här kommandot får integrerings konton från en resurs grupp som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3330c-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="3330c-117">Exempel 3: Hämta alla integrations konton</span><span class="sxs-lookup"><span data-stu-id="3330c-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="3330c-118">Det här kommandot får alla integrerings konton i din Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="3330c-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="3330c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3330c-119">PARAMETERS</span></span>

### <span data-ttu-id="3330c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3330c-120">-Name</span></span>
<span data-ttu-id="3330c-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="3330c-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3330c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3330c-122">-ResourceGroupName</span></span>
<span data-ttu-id="3330c-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3330c-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3330c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3330c-124">-DefaultProfile</span></span>
<span data-ttu-id="3330c-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3330c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3330c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3330c-126">CommonParameters</span></span>
<span data-ttu-id="3330c-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3330c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3330c-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3330c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3330c-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3330c-129">INPUTS</span></span>

## <span data-ttu-id="3330c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3330c-130">OUTPUTS</span></span>

### <span data-ttu-id="3330c-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3330c-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="3330c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3330c-132">NOTES</span></span>

## <span data-ttu-id="3330c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3330c-133">RELATED LINKS</span></span>

[<span data-ttu-id="3330c-134">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="3330c-134">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="3330c-135">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3330c-135">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="3330c-136">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3330c-136">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="3330c-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3330c-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


