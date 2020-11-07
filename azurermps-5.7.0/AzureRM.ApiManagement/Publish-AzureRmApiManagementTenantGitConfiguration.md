---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/publish-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3879def437171e9de2cad6f328ef6bf15bed3d48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576643"
---
# <span data-ttu-id="bb617-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb617-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="bb617-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb617-102">SYNOPSIS</span></span>
<span data-ttu-id="bb617-103">Publicerar ändringar från en git-gren till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="bb617-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb617-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb617-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb617-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb617-105">DESCRIPTION</span></span>
<span data-ttu-id="bb617-106">Cmdleten **Publishing-AzureRmApiManagementTenantGitConfiguration** publicerar ändringarna från en git-gren till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="bb617-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="bb617-107">Du kan alternativt verifiera ändringarna i en git-gren utan att publicera.</span><span class="sxs-lookup"><span data-stu-id="bb617-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="bb617-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb617-108">EXAMPLES</span></span>

### <span data-ttu-id="bb617-109">Exempel 1: Distribuera git-ändringar</span><span class="sxs-lookup"><span data-stu-id="bb617-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="bb617-110">Det här kommandot publicerar ändringarna från den angivna grenen till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="bb617-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="bb617-111">Exempel 2: validera git-ändringar</span><span class="sxs-lookup"><span data-stu-id="bb617-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="bb617-112">Det här kommandot verifierar ändringarna i git-grenen mot konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="bb617-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="bb617-113">Ändringar publiceras inte.</span><span class="sxs-lookup"><span data-stu-id="bb617-113">It does not publish changes.</span></span>

## <span data-ttu-id="bb617-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb617-114">PARAMETERS</span></span>

### <span data-ttu-id="bb617-115">-Gren</span><span class="sxs-lookup"><span data-stu-id="bb617-115">-Branch</span></span>
<span data-ttu-id="bb617-116">Anger namnet på den git-gren från vilken denna cmdlet distribuerar konfigurationen till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="bb617-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb617-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bb617-117">-Context</span></span>
<span data-ttu-id="bb617-118">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bb617-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb617-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb617-119">-DefaultProfile</span></span>
<span data-ttu-id="bb617-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb617-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="bb617-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bb617-121">-Force</span></span>
<span data-ttu-id="bb617-122">Anger att den här cmdleten tar bort abonnemang till produkter som tas bort i den här uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="bb617-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb617-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb617-123">-PassThru</span></span>
<span data-ttu-id="bb617-124">Anger att den här cmdleten returnerar ett **PsApiManagementOperationResult** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bb617-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb617-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="bb617-125">-ValidateOnly</span></span>
<span data-ttu-id="bb617-126">Anger att denna cmdlet verifierar ändringarna i angiven git-gren.</span><span class="sxs-lookup"><span data-stu-id="bb617-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="bb617-127">Den publicerar inte till konfigurations databasen.</span><span class="sxs-lookup"><span data-stu-id="bb617-127">It does not publish to the configuration database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb617-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb617-128">-Confirm</span></span>
<span data-ttu-id="bb617-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb617-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb617-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb617-130">-WhatIf</span></span>
<span data-ttu-id="bb617-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb617-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb617-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb617-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb617-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb617-133">CommonParameters</span></span>
<span data-ttu-id="bb617-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb617-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb617-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb617-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb617-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb617-136">INPUTS</span></span>

### <span data-ttu-id="bb617-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="bb617-137">None</span></span>
<span data-ttu-id="bb617-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bb617-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb617-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb617-139">OUTPUTS</span></span>

### <span data-ttu-id="bb617-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="bb617-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="bb617-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb617-141">NOTES</span></span>

## <span data-ttu-id="bb617-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb617-142">RELATED LINKS</span></span>

[<span data-ttu-id="bb617-143">Spara – AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb617-143">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)

