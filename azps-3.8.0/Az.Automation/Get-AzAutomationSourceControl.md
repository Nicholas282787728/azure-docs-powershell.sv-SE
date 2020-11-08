---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092717"
---
# <span data-ttu-id="27f9a-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="27f9a-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="27f9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="27f9a-103">Hämtar en lista med käll kontroller för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="27f9a-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="27f9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27f9a-104">SYNTAX</span></span>

### <span data-ttu-id="27f9a-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="27f9a-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27f9a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="27f9a-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27f9a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27f9a-107">DESCRIPTION</span></span>
<span data-ttu-id="27f9a-108">Get-AzAutomationSourceControl cmdlet får kontroll för automatiserings källan.</span><span class="sxs-lookup"><span data-stu-id="27f9a-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="27f9a-109">Ange namnet på en specifik käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="27f9a-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="27f9a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27f9a-110">EXAMPLES</span></span>

### <span data-ttu-id="27f9a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="27f9a-111">Example 1</span></span>
<span data-ttu-id="27f9a-112">Det här kommandot får en kontroll för en automatiserings källa med namnet VSTSNative i kontot som heter devAccount.</span><span class="sxs-lookup"><span data-stu-id="27f9a-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="27f9a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27f9a-113">PARAMETERS</span></span>

### <span data-ttu-id="27f9a-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="27f9a-114">-AutomationAccountName</span></span>
<span data-ttu-id="27f9a-115">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="27f9a-115">The automation account name.</span></span>

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

### <span data-ttu-id="27f9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27f9a-116">-DefaultProfile</span></span>
<span data-ttu-id="27f9a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="27f9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27f9a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="27f9a-118">-Name</span></span>
<span data-ttu-id="27f9a-119">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="27f9a-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27f9a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27f9a-120">-ResourceGroupName</span></span>
<span data-ttu-id="27f9a-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="27f9a-121">The resource group name.</span></span>

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

### <span data-ttu-id="27f9a-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="27f9a-122">-SourceType</span></span>
<span data-ttu-id="27f9a-123">Käll kontroll typen.</span><span class="sxs-lookup"><span data-stu-id="27f9a-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27f9a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27f9a-124">CommonParameters</span></span>
<span data-ttu-id="27f9a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27f9a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27f9a-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27f9a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27f9a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27f9a-127">INPUTS</span></span>

### <span data-ttu-id="27f9a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="27f9a-128">System.String</span></span>

## <span data-ttu-id="27f9a-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27f9a-129">OUTPUTS</span></span>

### <span data-ttu-id="27f9a-130">Microsoft. Azure. commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="27f9a-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="27f9a-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27f9a-131">NOTES</span></span>

## <span data-ttu-id="27f9a-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27f9a-132">RELATED LINKS</span></span>
