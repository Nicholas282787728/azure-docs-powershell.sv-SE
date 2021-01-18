---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525946"
---
# <span data-ttu-id="ca2d3-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ca2d3-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="ca2d3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca2d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca2d3-103">Hämtar integrerings konton.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-103">Gets integration accounts.</span></span>

## <span data-ttu-id="ca2d3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca2d3-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca2d3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca2d3-105">DESCRIPTION</span></span>
<span data-ttu-id="ca2d3-106">Cmdleten **Get-AzIntegrationAccount** hämtar integrerings konton från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="ca2d3-107">Ange namnet på integrations kontot och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="ca2d3-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ca2d3-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ca2d3-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ca2d3-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ca2d3-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca2d3-112">EXAMPLES</span></span>

### <span data-ttu-id="ca2d3-113">Exempel 1: skaffa ett integrations konto efter namn</span><span class="sxs-lookup"><span data-stu-id="ca2d3-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="ca2d3-114">Det här kommandot får ett integrerings konto med namnet IntegrationAccount31 från den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="ca2d3-115">Exempel 2: skaffa integrerings konton i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ca2d3-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="ca2d3-116">Det här kommandot får integrerings konton från en resurs grupp som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ca2d3-117">Exempel 3: Hämta alla integrations konton</span><span class="sxs-lookup"><span data-stu-id="ca2d3-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="ca2d3-118">Det här kommandot får alla integrerings konton i din Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="ca2d3-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca2d3-119">PARAMETERS</span></span>

### <span data-ttu-id="ca2d3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca2d3-120">-DefaultProfile</span></span>
<span data-ttu-id="ca2d3-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ca2d3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca2d3-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca2d3-122">-Name</span></span>
<span data-ttu-id="ca2d3-123">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ca2d3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca2d3-124">-ResourceGroupName</span></span>
<span data-ttu-id="ca2d3-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ca2d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca2d3-126">CommonParameters</span></span>
<span data-ttu-id="ca2d3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca2d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca2d3-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca2d3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca2d3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca2d3-129">INPUTS</span></span>

### <span data-ttu-id="ca2d3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ca2d3-130">System.String</span></span>

## <span data-ttu-id="ca2d3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca2d3-131">OUTPUTS</span></span>

### <span data-ttu-id="ca2d3-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ca2d3-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="ca2d3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca2d3-133">NOTES</span></span>

## <span data-ttu-id="ca2d3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca2d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="ca2d3-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ca2d3-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="ca2d3-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ca2d3-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="ca2d3-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ca2d3-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="ca2d3-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ca2d3-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


