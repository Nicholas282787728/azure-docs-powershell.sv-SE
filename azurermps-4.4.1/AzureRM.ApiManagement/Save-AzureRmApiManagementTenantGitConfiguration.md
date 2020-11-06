---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 91cd7855b832a406fdd3ce9a959135936ee3c284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583876"
---
# <span data-ttu-id="fab77-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="fab77-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="fab77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fab77-102">SYNOPSIS</span></span>
<span data-ttu-id="fab77-103">Sparar ändringar genom att skapa en aktuell konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fab77-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fab77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fab77-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fab77-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fab77-105">DESCRIPTION</span></span>
<span data-ttu-id="fab77-106">Cmdleten **Save-AzureRmApiManagementTenantGitConfiguration** sparar ändringarna genom att skapa ett bekräftelse som innehåller den aktuella konfigurationen ögonblicks bilden till en gren i databasen.</span><span class="sxs-lookup"><span data-stu-id="fab77-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="fab77-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fab77-107">EXAMPLES</span></span>

### <span data-ttu-id="fab77-108">Exempel 1: Spara ändringar i konfigurationen</span><span class="sxs-lookup"><span data-stu-id="fab77-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="fab77-109">Det här kommandot sparar ändringarna genom att skapa en bekräftelse med den aktuella konfigurationen ögonblicks bild till den angivna grenen i databasen.</span><span class="sxs-lookup"><span data-stu-id="fab77-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="fab77-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fab77-110">PARAMETERS</span></span>

### <span data-ttu-id="fab77-111">-Gren</span><span class="sxs-lookup"><span data-stu-id="fab77-111">-Branch</span></span>
<span data-ttu-id="fab77-112">Anger namnet på git-grenen där du vill att den aktuella konfigurationen ska genomföras.</span><span class="sxs-lookup"><span data-stu-id="fab77-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="fab77-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fab77-113">-Context</span></span>
<span data-ttu-id="fab77-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fab77-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fab77-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fab77-115">-Force</span></span>
<span data-ttu-id="fab77-116">Anger att den här cmdleten bekräftar den aktuella konfigurations databasen för git-databasen, även om den git-databasen har nyare ändringar som skrivs över.</span><span class="sxs-lookup"><span data-stu-id="fab77-116">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="fab77-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fab77-117">-PassThru</span></span>
<span data-ttu-id="fab77-118">Anger att den här cmdleten returnerar ett **PsApiManagementOperationResult** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fab77-118">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="fab77-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fab77-119">-Confirm</span></span>
<span data-ttu-id="fab77-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fab77-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab77-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab77-121">-WhatIf</span></span>
<span data-ttu-id="fab77-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fab77-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab77-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fab77-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab77-124">-DefaultProfile</span></span>
<span data-ttu-id="fab77-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fab77-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fab77-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab77-126">CommonParameters</span></span>
<span data-ttu-id="fab77-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab77-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab77-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab77-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab77-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fab77-129">INPUTS</span></span>

## <span data-ttu-id="fab77-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fab77-130">OUTPUTS</span></span>

### <span data-ttu-id="fab77-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="fab77-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="fab77-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fab77-132">NOTES</span></span>

## <span data-ttu-id="fab77-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fab77-133">RELATED LINKS</span></span>

[<span data-ttu-id="fab77-134">Publicera – AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="fab77-134">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


