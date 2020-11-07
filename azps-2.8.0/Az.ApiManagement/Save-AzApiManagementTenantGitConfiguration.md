---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 1caabfbf5c3139f27b44f8ccad3612eb34f36fd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745686"
---
# <span data-ttu-id="4250b-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="4250b-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="4250b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4250b-102">SYNOPSIS</span></span>
<span data-ttu-id="4250b-103">Sparar ändringar genom att skapa en aktuell konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4250b-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="4250b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4250b-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4250b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4250b-105">DESCRIPTION</span></span>
<span data-ttu-id="4250b-106">Cmdleten **Save-AzApiManagementTenantGitConfiguration** sparar ändringarna genom att skapa ett bekräftelse som innehåller den aktuella konfigurationen ögonblicks bilden till en gren i databasen.</span><span class="sxs-lookup"><span data-stu-id="4250b-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="4250b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4250b-107">EXAMPLES</span></span>

### <span data-ttu-id="4250b-108">Exempel 1: Spara ändringar i konfigurationen</span><span class="sxs-lookup"><span data-stu-id="4250b-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="4250b-109">Det här kommandot sparar ändringarna genom att skapa en bekräftelse med den aktuella konfigurationen ögonblicks bild till den angivna grenen i databasen.</span><span class="sxs-lookup"><span data-stu-id="4250b-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="4250b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4250b-110">PARAMETERS</span></span>

### <span data-ttu-id="4250b-111">-Gren</span><span class="sxs-lookup"><span data-stu-id="4250b-111">-Branch</span></span>
<span data-ttu-id="4250b-112">Anger namnet på git-grenen där du vill att den aktuella konfigurationen ska genomföras.</span><span class="sxs-lookup"><span data-stu-id="4250b-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="4250b-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4250b-113">-Context</span></span>
<span data-ttu-id="4250b-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4250b-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4250b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4250b-115">-DefaultProfile</span></span>
<span data-ttu-id="4250b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4250b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4250b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4250b-117">-Force</span></span>
<span data-ttu-id="4250b-118">Anger att den här cmdleten bekräftar den aktuella konfigurations databasen för git-databasen, även om den git-databasen har nyare ändringar som skrivs över.</span><span class="sxs-lookup"><span data-stu-id="4250b-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="4250b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4250b-119">-PassThru</span></span>
<span data-ttu-id="4250b-120">Anger att den här cmdleten returnerar ett **PsApiManagementOperationResult** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4250b-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="4250b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4250b-121">-Confirm</span></span>
<span data-ttu-id="4250b-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4250b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4250b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4250b-123">-WhatIf</span></span>
<span data-ttu-id="4250b-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4250b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4250b-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4250b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4250b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4250b-126">CommonParameters</span></span>
<span data-ttu-id="4250b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4250b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4250b-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4250b-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4250b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4250b-129">INPUTS</span></span>

### <span data-ttu-id="4250b-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4250b-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4250b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4250b-131">System.String</span></span>

### <span data-ttu-id="4250b-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4250b-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4250b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4250b-133">OUTPUTS</span></span>

### <span data-ttu-id="4250b-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="4250b-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="4250b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4250b-135">NOTES</span></span>

## <span data-ttu-id="4250b-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4250b-136">RELATED LINKS</span></span>

[<span data-ttu-id="4250b-137">Publicera – AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="4250b-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


