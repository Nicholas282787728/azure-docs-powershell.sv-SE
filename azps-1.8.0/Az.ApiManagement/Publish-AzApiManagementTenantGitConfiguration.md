---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 26f5be9ff3ec8d1a8b117bcaefd425047cd897ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917821"
---
# <span data-ttu-id="587cf-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="587cf-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="587cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="587cf-102">SYNOPSIS</span></span>
<span data-ttu-id="587cf-103">Publicerar ändringar från en git-gren till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="587cf-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="587cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="587cf-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="587cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="587cf-105">DESCRIPTION</span></span>
<span data-ttu-id="587cf-106">Cmdleten **Publishing-AzApiManagementTenantGitConfiguration** publicerar ändringarna från en git-gren till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="587cf-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="587cf-107">Du kan alternativt verifiera ändringarna i en git-gren utan att publicera.</span><span class="sxs-lookup"><span data-stu-id="587cf-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="587cf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="587cf-108">EXAMPLES</span></span>

### <span data-ttu-id="587cf-109">Exempel 1: Distribuera git-ändringar</span><span class="sxs-lookup"><span data-stu-id="587cf-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="587cf-110">Det här kommandot publicerar ändringarna från den angivna grenen till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="587cf-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="587cf-111">Exempel 2: validera git-ändringar</span><span class="sxs-lookup"><span data-stu-id="587cf-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="587cf-112">Det här kommandot verifierar ändringarna i git-grenen mot konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="587cf-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="587cf-113">Ändringar publiceras inte.</span><span class="sxs-lookup"><span data-stu-id="587cf-113">It does not publish changes.</span></span>

## <span data-ttu-id="587cf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="587cf-114">PARAMETERS</span></span>

### <span data-ttu-id="587cf-115">-Gren</span><span class="sxs-lookup"><span data-stu-id="587cf-115">-Branch</span></span>
<span data-ttu-id="587cf-116">Anger namnet på den git-gren från vilken denna cmdlet distribuerar konfigurationen till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="587cf-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587cf-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="587cf-117">-Context</span></span>
<span data-ttu-id="587cf-118">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="587cf-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587cf-119">-DefaultProfile</span></span>
<span data-ttu-id="587cf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="587cf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="587cf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="587cf-121">-Force</span></span>
<span data-ttu-id="587cf-122">Anger att den här cmdleten tar bort abonnemang till produkter som tas bort i den här uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="587cf-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587cf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="587cf-123">-PassThru</span></span>
<span data-ttu-id="587cf-124">Anger att den här cmdleten returnerar ett **PsApiManagementOperationResult** -objekt.</span><span class="sxs-lookup"><span data-stu-id="587cf-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587cf-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="587cf-125">-ValidateOnly</span></span>
<span data-ttu-id="587cf-126">Anger att denna cmdlet verifierar ändringarna i angiven git-gren.</span><span class="sxs-lookup"><span data-stu-id="587cf-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="587cf-127">Den publicerar inte till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="587cf-127">It does not publish to the configuration database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587cf-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="587cf-128">-Confirm</span></span>
<span data-ttu-id="587cf-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="587cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="587cf-130">-WhatIf</span></span>
<span data-ttu-id="587cf-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="587cf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="587cf-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="587cf-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="587cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587cf-133">CommonParameters</span></span>
<span data-ttu-id="587cf-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="587cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587cf-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="587cf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587cf-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="587cf-136">INPUTS</span></span>

### <span data-ttu-id="587cf-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="587cf-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="587cf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="587cf-138">System.String</span></span>

### <span data-ttu-id="587cf-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="587cf-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="587cf-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="587cf-140">OUTPUTS</span></span>

### <span data-ttu-id="587cf-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="587cf-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="587cf-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="587cf-142">NOTES</span></span>

## <span data-ttu-id="587cf-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="587cf-143">RELATED LINKS</span></span>

[<span data-ttu-id="587cf-144">Spara – AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="587cf-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


