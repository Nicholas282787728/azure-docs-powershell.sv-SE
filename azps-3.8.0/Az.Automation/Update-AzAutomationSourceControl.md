---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: ee3b7b7cdbe098c6892782ca4084bd2fb7e6a615
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926893"
---
# <span data-ttu-id="d564c-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="d564c-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="d564c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d564c-102">SYNOPSIS</span></span>
<span data-ttu-id="d564c-103">Uppdaterar en käll kontroll för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d564c-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="d564c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d564c-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d564c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d564c-105">DESCRIPTION</span></span>
<span data-ttu-id="d564c-106">Den Update-AzAutomationSourceControl cmdleten ändrar värdet för ett fält i en käll kontroll i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d564c-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="d564c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d564c-107">EXAMPLES</span></span>

### <span data-ttu-id="d564c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d564c-108">Example 1</span></span>
<span data-ttu-id="d564c-109">Med det här kommandot anges fältet PublishRunbook till falskt för Azure Automation Source Control med namnet VSTSNative i kontot som heter devAccount.</span><span class="sxs-lookup"><span data-stu-id="d564c-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="d564c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d564c-110">PARAMETERS</span></span>

### <span data-ttu-id="d564c-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="d564c-111">-AccessToken</span></span>
<span data-ttu-id="d564c-112">Åtkomst till käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="d564c-112">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d564c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d564c-113">-AutomationAccountName</span></span>
<span data-ttu-id="d564c-114">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="d564c-114">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d564c-115">-Automatisk synkronisering</span><span class="sxs-lookup"><span data-stu-id="d564c-115">-AutoSync</span></span>
<span data-ttu-id="d564c-116">Egenskapen AutoSync för käll kontrollen.</span><span class="sxs-lookup"><span data-stu-id="d564c-116">The autoSync property for the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d564c-117">-Gren</span><span class="sxs-lookup"><span data-stu-id="d564c-117">-Branch</span></span>
<span data-ttu-id="d564c-118">Käll kontrolls grenen.</span><span class="sxs-lookup"><span data-stu-id="d564c-118">The source control branch.</span></span>

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

### <span data-ttu-id="d564c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d564c-119">-DefaultProfile</span></span>
<span data-ttu-id="d564c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d564c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d564c-121">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d564c-121">-Description</span></span>
<span data-ttu-id="d564c-122">Käll kontroll beskrivningen.</span><span class="sxs-lookup"><span data-stu-id="d564c-122">The source control description.</span></span>

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

### <span data-ttu-id="d564c-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="d564c-123">-FolderPath</span></span>
<span data-ttu-id="d564c-124">Sökvägen till käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="d564c-124">The source control folder path.</span></span>

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

### <span data-ttu-id="d564c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="d564c-125">-Name</span></span>
<span data-ttu-id="d564c-126">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="d564c-126">The source control name.</span></span>

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

### <span data-ttu-id="d564c-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="d564c-127">-PublishRunbook</span></span>
<span data-ttu-id="d564c-128">Egenskapen publishRunbook för käll kontrollen.</span><span class="sxs-lookup"><span data-stu-id="d564c-128">The publishRunbook property of the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d564c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d564c-129">-ResourceGroupName</span></span>
<span data-ttu-id="d564c-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d564c-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d564c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d564c-131">-Confirm</span></span>
<span data-ttu-id="d564c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d564c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d564c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d564c-133">-WhatIf</span></span>
<span data-ttu-id="d564c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d564c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d564c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d564c-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d564c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d564c-136">CommonParameters</span></span>
<span data-ttu-id="d564c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d564c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d564c-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d564c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d564c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d564c-139">INPUTS</span></span>

### <span data-ttu-id="d564c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d564c-140">System.String</span></span>

## <span data-ttu-id="d564c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d564c-141">OUTPUTS</span></span>

### <span data-ttu-id="d564c-142">Microsoft. Azure. commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="d564c-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="d564c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d564c-143">NOTES</span></span>

## <span data-ttu-id="d564c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d564c-144">RELATED LINKS</span></span>
