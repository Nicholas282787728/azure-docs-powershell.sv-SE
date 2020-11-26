---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3995506c302d2993623f12fcb7e6e2b9f96fd208
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258385"
---
# <span data-ttu-id="f15aa-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="f15aa-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="f15aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f15aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f15aa-103">Sparar ändringar genom att skapa en aktuell konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f15aa-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="f15aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f15aa-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f15aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f15aa-105">DESCRIPTION</span></span>
<span data-ttu-id="f15aa-106">Cmdleten **Save-AzApiManagementTenantGitConfiguration** sparar ändringarna genom att skapa ett bekräftelse som innehåller den aktuella konfigurationen ögonblicks bilden till en gren i databasen.</span><span class="sxs-lookup"><span data-stu-id="f15aa-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="f15aa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f15aa-107">EXAMPLES</span></span>

### <span data-ttu-id="f15aa-108">Exempel 1: Spara ändringar i konfigurationen</span><span class="sxs-lookup"><span data-stu-id="f15aa-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="f15aa-109">Det här kommandot sparar ändringarna genom att skapa en bekräftelse med den aktuella konfigurationen ögonblicks bild till den angivna grenen i databasen.</span><span class="sxs-lookup"><span data-stu-id="f15aa-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="f15aa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f15aa-110">PARAMETERS</span></span>

### <span data-ttu-id="f15aa-111">-Gren</span><span class="sxs-lookup"><span data-stu-id="f15aa-111">-Branch</span></span>
<span data-ttu-id="f15aa-112">Anger namnet på git-grenen där du vill att den aktuella konfigurationen ska genomföras.</span><span class="sxs-lookup"><span data-stu-id="f15aa-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="f15aa-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f15aa-113">-Context</span></span>
<span data-ttu-id="f15aa-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f15aa-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f15aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15aa-115">-DefaultProfile</span></span>
<span data-ttu-id="f15aa-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f15aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f15aa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f15aa-117">-Force</span></span>
<span data-ttu-id="f15aa-118">Anger att den här cmdleten bekräftar den aktuella konfigurations databasen för git-databasen, även om den git-databasen har nyare ändringar som skrivs över.</span><span class="sxs-lookup"><span data-stu-id="f15aa-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="f15aa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f15aa-119">-PassThru</span></span>
<span data-ttu-id="f15aa-120">Anger att den här cmdleten returnerar ett **PsApiManagementOperationResult** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f15aa-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="f15aa-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f15aa-121">-Confirm</span></span>
<span data-ttu-id="f15aa-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f15aa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f15aa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f15aa-123">-WhatIf</span></span>
<span data-ttu-id="f15aa-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f15aa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f15aa-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f15aa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f15aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15aa-126">CommonParameters</span></span>
<span data-ttu-id="f15aa-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f15aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15aa-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f15aa-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15aa-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f15aa-129">INPUTS</span></span>

### <span data-ttu-id="f15aa-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f15aa-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f15aa-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f15aa-131">System.String</span></span>

### <span data-ttu-id="f15aa-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f15aa-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f15aa-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f15aa-133">OUTPUTS</span></span>

### <span data-ttu-id="f15aa-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="f15aa-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="f15aa-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f15aa-135">NOTES</span></span>

## <span data-ttu-id="f15aa-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f15aa-136">RELATED LINKS</span></span>

[<span data-ttu-id="f15aa-137">Publicera – AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="f15aa-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)

