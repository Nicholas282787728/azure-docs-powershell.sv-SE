---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSourceControl.md
ms.openlocfilehash: abd09a195db5652d2dfdffce17096116895eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575349"
---
# <span data-ttu-id="dd627-101">Remove-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="dd627-101">Remove-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="dd627-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd627-102">SYNOPSIS</span></span>
<span data-ttu-id="dd627-103">Tar bort en Azure Automation-källkod.</span><span class="sxs-lookup"><span data-stu-id="dd627-103">Removes an Azure Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd627-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd627-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd627-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd627-105">DESCRIPTION</span></span>
<span data-ttu-id="dd627-106">Remove-AzureRmAutomationSourceControl cmdlet tar bort en käll kontroll från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="dd627-106">The Remove-AzureRmAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="dd627-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd627-107">EXAMPLES</span></span>

### <span data-ttu-id="dd627-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd627-108">Example 1</span></span>
<span data-ttu-id="dd627-109">Det här kommandot tar bort Automation Source Control med namnet VSTSNative i kontot som heter devAccount.</span><span class="sxs-lookup"><span data-stu-id="dd627-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="dd627-110">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="dd627-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="dd627-111">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="dd627-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="dd627-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd627-112">PARAMETERS</span></span>

### <span data-ttu-id="dd627-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd627-113">-AutomationAccountName</span></span>
<span data-ttu-id="dd627-114">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="dd627-114">The automation account name.</span></span>

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

### <span data-ttu-id="dd627-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd627-115">-DefaultProfile</span></span>
<span data-ttu-id="dd627-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd627-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd627-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd627-117">-Name</span></span>
<span data-ttu-id="dd627-118">Namn på käll kontroll.</span><span class="sxs-lookup"><span data-stu-id="dd627-118">The source control name.</span></span>

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

### <span data-ttu-id="dd627-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd627-119">-PassThru</span></span>
<span data-ttu-id="dd627-120">PassThru returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="dd627-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd627-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="dd627-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd627-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd627-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd627-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="dd627-123">The resource group name.</span></span>

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

### <span data-ttu-id="dd627-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd627-124">-Confirm</span></span>
<span data-ttu-id="dd627-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd627-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd627-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd627-126">-WhatIf</span></span>
<span data-ttu-id="dd627-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd627-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd627-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd627-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd627-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd627-129">CommonParameters</span></span>
<span data-ttu-id="dd627-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd627-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd627-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd627-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd627-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd627-132">INPUTS</span></span>

### <span data-ttu-id="dd627-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dd627-133">System.String</span></span>

## <span data-ttu-id="dd627-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd627-134">OUTPUTS</span></span>

### <span data-ttu-id="dd627-135">Microsoft. Azure. commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="dd627-135">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="dd627-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd627-136">NOTES</span></span>

## <span data-ttu-id="dd627-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd627-137">RELATED LINKS</span></span>
