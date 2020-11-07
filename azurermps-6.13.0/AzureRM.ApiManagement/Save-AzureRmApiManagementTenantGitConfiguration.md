---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/save-azurermapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 9b297771f05b35493f8a852fd6d3450d2b5e7531
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756734"
---
# <span data-ttu-id="6acbe-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="6acbe-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="6acbe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6acbe-102">SYNOPSIS</span></span>
<span data-ttu-id="6acbe-103">Sparar ändringar genom att skapa en aktuell konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6acbe-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6acbe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6acbe-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6acbe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6acbe-105">DESCRIPTION</span></span>
<span data-ttu-id="6acbe-106">Cmdleten **Save-AzureRmApiManagementTenantGitConfiguration** sparar ändringarna genom att skapa ett bekräftelse som innehåller den aktuella konfigurationen ögonblicks bilden till en gren i databasen.</span><span class="sxs-lookup"><span data-stu-id="6acbe-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="6acbe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6acbe-107">EXAMPLES</span></span>

### <span data-ttu-id="6acbe-108">Exempel 1: Spara ändringar i konfigurationen</span><span class="sxs-lookup"><span data-stu-id="6acbe-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="6acbe-109">Det här kommandot sparar ändringarna genom att skapa en bekräftelse med den aktuella konfigurationen ögonblicks bild till den angivna grenen i databasen.</span><span class="sxs-lookup"><span data-stu-id="6acbe-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="6acbe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6acbe-110">PARAMETERS</span></span>

### <span data-ttu-id="6acbe-111">-Gren</span><span class="sxs-lookup"><span data-stu-id="6acbe-111">-Branch</span></span>
<span data-ttu-id="6acbe-112">Anger namnet på git-grenen där du vill att den aktuella konfigurationen ska genomföras.</span><span class="sxs-lookup"><span data-stu-id="6acbe-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="6acbe-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6acbe-113">-Context</span></span>
<span data-ttu-id="6acbe-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6acbe-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6acbe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6acbe-115">-DefaultProfile</span></span>
<span data-ttu-id="6acbe-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6acbe-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6acbe-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6acbe-117">-Force</span></span>
<span data-ttu-id="6acbe-118">Anger att den här cmdleten bekräftar den aktuella konfigurations databasen för git-databasen, även om den git-databasen har nyare ändringar som skrivs över.</span><span class="sxs-lookup"><span data-stu-id="6acbe-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="6acbe-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6acbe-119">-PassThru</span></span>
<span data-ttu-id="6acbe-120">Anger att den här cmdleten returnerar ett **PsApiManagementOperationResult** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6acbe-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="6acbe-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6acbe-121">-Confirm</span></span>
<span data-ttu-id="6acbe-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6acbe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6acbe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6acbe-123">-WhatIf</span></span>
<span data-ttu-id="6acbe-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6acbe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6acbe-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6acbe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6acbe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6acbe-126">CommonParameters</span></span>
<span data-ttu-id="6acbe-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6acbe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6acbe-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6acbe-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6acbe-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6acbe-129">INPUTS</span></span>

### <span data-ttu-id="6acbe-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6acbe-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6acbe-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6acbe-131">System.String</span></span>

### <span data-ttu-id="6acbe-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6acbe-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6acbe-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6acbe-133">OUTPUTS</span></span>

### <span data-ttu-id="6acbe-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="6acbe-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="6acbe-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6acbe-135">NOTES</span></span>

## <span data-ttu-id="6acbe-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6acbe-136">RELATED LINKS</span></span>

[<span data-ttu-id="6acbe-137">Publicera – AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="6acbe-137">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


