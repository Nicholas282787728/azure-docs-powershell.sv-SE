---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: 9c60e9171385c915785c87d5de217b76a37a4862
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743798"
---
# <span data-ttu-id="e7b24-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="e7b24-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="e7b24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7b24-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b24-103">Hämtar schema för integrerings konton.</span><span class="sxs-lookup"><span data-stu-id="e7b24-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="e7b24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7b24-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7b24-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7b24-105">DESCRIPTION</span></span>
<span data-ttu-id="e7b24-106">Cmdleten **Get-AzIntegrationAccountSchema** hämtar ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="e7b24-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="e7b24-107">Ange integrerings konto namn, resurs grupps namn och schema namn.</span><span class="sxs-lookup"><span data-stu-id="e7b24-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="e7b24-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="e7b24-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e7b24-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="e7b24-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e7b24-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="e7b24-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e7b24-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="e7b24-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e7b24-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7b24-112">EXAMPLES</span></span>

### <span data-ttu-id="e7b24-113">Exempel 1: skaffa ett integrations konto schema</span><span class="sxs-lookup"><span data-stu-id="e7b24-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="e7b24-114">Det här kommandot får integrerings kontots schema med namnet IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="e7b24-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="e7b24-115">Exempel 2: skaffa ett integrations konto schema för en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="e7b24-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="e7b24-116">Det här kommandot får integrerings konto scheman för resurs gruppen "ResourceGroup11".</span><span class="sxs-lookup"><span data-stu-id="e7b24-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e7b24-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7b24-117">PARAMETERS</span></span>

### <span data-ttu-id="e7b24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b24-118">-DefaultProfile</span></span>
<span data-ttu-id="e7b24-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e7b24-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7b24-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e7b24-120">-Name</span></span>
<span data-ttu-id="e7b24-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="e7b24-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="e7b24-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b24-122">-ResourceGroupName</span></span>
<span data-ttu-id="e7b24-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e7b24-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e7b24-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e7b24-124">-SchemaName</span></span>
<span data-ttu-id="e7b24-125">Anger namnet på ett integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="e7b24-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="e7b24-126">Anger namnet på ett schema.</span><span class="sxs-lookup"><span data-stu-id="e7b24-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="e7b24-127">.</span><span class="sxs-lookup"><span data-stu-id="e7b24-127">.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b24-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b24-128">CommonParameters</span></span>
<span data-ttu-id="e7b24-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7b24-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b24-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b24-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b24-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7b24-131">INPUTS</span></span>

### <span data-ttu-id="e7b24-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e7b24-132">System.String</span></span>

## <span data-ttu-id="e7b24-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7b24-133">OUTPUTS</span></span>

### <span data-ttu-id="e7b24-134">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="e7b24-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="e7b24-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7b24-135">NOTES</span></span>

## <span data-ttu-id="e7b24-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7b24-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7b24-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="e7b24-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="e7b24-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="e7b24-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="e7b24-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="e7b24-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


