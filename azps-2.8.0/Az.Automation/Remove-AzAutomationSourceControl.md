---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: 165850e0212969fea76e85f209d3fcf7c2040b79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745483"
---
# <span data-ttu-id="ed557-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="ed557-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="ed557-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed557-102">SYNOPSIS</span></span>
<span data-ttu-id="ed557-103">Tar bort en Azure Automation-källkod.</span><span class="sxs-lookup"><span data-stu-id="ed557-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="ed557-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed557-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed557-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed557-105">DESCRIPTION</span></span>
<span data-ttu-id="ed557-106">Remove-AzAutomationSourceControl cmdlet tar bort en käll kontroll från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ed557-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="ed557-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed557-107">EXAMPLES</span></span>

### <span data-ttu-id="ed557-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ed557-108">Example 1</span></span>
<span data-ttu-id="ed557-109">Det här kommandot tar bort Automation Source Control med namnet VSTSNative i kontot som heter devAccount.</span><span class="sxs-lookup"><span data-stu-id="ed557-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="ed557-110">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="ed557-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="ed557-111">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ed557-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="ed557-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed557-112">PARAMETERS</span></span>

### <span data-ttu-id="ed557-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed557-113">-AutomationAccountName</span></span>
<span data-ttu-id="ed557-114">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="ed557-114">The automation account name.</span></span>

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

### <span data-ttu-id="ed557-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed557-115">-DefaultProfile</span></span>
<span data-ttu-id="ed557-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed557-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed557-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed557-117">-Name</span></span>
<span data-ttu-id="ed557-118">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="ed557-118">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed557-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed557-119">-PassThru</span></span>
<span data-ttu-id="ed557-120">PassThru returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ed557-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed557-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ed557-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed557-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed557-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed557-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ed557-123">The resource group name.</span></span>

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

### <span data-ttu-id="ed557-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed557-124">-Confirm</span></span>
<span data-ttu-id="ed557-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed557-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed557-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed557-126">-WhatIf</span></span>
<span data-ttu-id="ed557-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed557-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed557-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed557-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed557-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed557-129">CommonParameters</span></span>
<span data-ttu-id="ed557-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed557-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed557-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed557-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed557-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed557-132">INPUTS</span></span>

### <span data-ttu-id="ed557-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ed557-133">System.String</span></span>

## <span data-ttu-id="ed557-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed557-134">OUTPUTS</span></span>

### <span data-ttu-id="ed557-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="ed557-135">System.Void</span></span>

### <span data-ttu-id="ed557-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed557-136">System.Boolean</span></span>

## <span data-ttu-id="ed557-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed557-137">NOTES</span></span>

## <span data-ttu-id="ed557-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed557-138">RELATED LINKS</span></span>
