---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: b9963fc53a146a2e8c76ac9b15166f0de6ba67ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745739"
---
# <span data-ttu-id="89348-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="89348-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="89348-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89348-102">SYNOPSIS</span></span>
<span data-ttu-id="89348-103">Publicerar ändringar från en git-gren till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="89348-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="89348-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89348-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89348-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89348-105">DESCRIPTION</span></span>
<span data-ttu-id="89348-106">Cmdleten **Publishing-AzApiManagementTenantGitConfiguration** publicerar ändringarna från en git-gren till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="89348-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="89348-107">Du kan alternativt verifiera ändringarna i en git-gren utan att publicera.</span><span class="sxs-lookup"><span data-stu-id="89348-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="89348-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89348-108">EXAMPLES</span></span>

### <span data-ttu-id="89348-109">Exempel 1: Distribuera git-ändringar</span><span class="sxs-lookup"><span data-stu-id="89348-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="89348-110">Det här kommandot publicerar ändringarna från den angivna grenen till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="89348-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="89348-111">Exempel 2: validera git-ändringar</span><span class="sxs-lookup"><span data-stu-id="89348-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="89348-112">Det här kommandot verifierar ändringarna i git-grenen mot konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="89348-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="89348-113">Ändringar publiceras inte.</span><span class="sxs-lookup"><span data-stu-id="89348-113">It does not publish changes.</span></span>

## <span data-ttu-id="89348-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89348-114">PARAMETERS</span></span>

### <span data-ttu-id="89348-115">-Gren</span><span class="sxs-lookup"><span data-stu-id="89348-115">-Branch</span></span>
<span data-ttu-id="89348-116">Anger namnet på den git-gren från vilken denna cmdlet distribuerar konfigurationen till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="89348-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="89348-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="89348-117">-Context</span></span>
<span data-ttu-id="89348-118">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="89348-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="89348-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89348-119">-DefaultProfile</span></span>
<span data-ttu-id="89348-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89348-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89348-121">-Force</span><span class="sxs-lookup"><span data-stu-id="89348-121">-Force</span></span>
<span data-ttu-id="89348-122">Anger att den här cmdleten tar bort abonnemang till produkter som tas bort i den här uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="89348-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="89348-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89348-123">-PassThru</span></span>
<span data-ttu-id="89348-124">Anger att den här cmdleten returnerar ett **PsApiManagementOperationResult** -objekt.</span><span class="sxs-lookup"><span data-stu-id="89348-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="89348-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="89348-125">-ValidateOnly</span></span>
<span data-ttu-id="89348-126">Anger att denna cmdlet verifierar ändringarna i angiven git-gren.</span><span class="sxs-lookup"><span data-stu-id="89348-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="89348-127">Den publicerar inte till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="89348-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="89348-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89348-128">-Confirm</span></span>
<span data-ttu-id="89348-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89348-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89348-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89348-130">-WhatIf</span></span>
<span data-ttu-id="89348-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89348-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89348-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89348-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89348-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89348-133">CommonParameters</span></span>
<span data-ttu-id="89348-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89348-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89348-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89348-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89348-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89348-136">INPUTS</span></span>

### <span data-ttu-id="89348-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="89348-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="89348-138">System. String</span><span class="sxs-lookup"><span data-stu-id="89348-138">System.String</span></span>

### <span data-ttu-id="89348-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89348-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="89348-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89348-140">OUTPUTS</span></span>

### <span data-ttu-id="89348-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="89348-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="89348-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89348-142">NOTES</span></span>

## <span data-ttu-id="89348-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89348-143">RELATED LINKS</span></span>

[<span data-ttu-id="89348-144">Spara – AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="89348-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


