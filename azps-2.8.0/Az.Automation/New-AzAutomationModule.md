---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 7e9b2e9a87cc9a02c807a2eae3b64e7a13c87a1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745525"
---
# <span data-ttu-id="246c3-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="246c3-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="246c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="246c3-102">SYNOPSIS</span></span>
<span data-ttu-id="246c3-103">Importerar en modul till Automation.</span><span class="sxs-lookup"><span data-stu-id="246c3-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="246c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="246c3-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="246c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="246c3-105">DESCRIPTION</span></span>
<span data-ttu-id="246c3-106">Cmdleten **New-AzAutomationModule** importerar en modul till Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="246c3-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="246c3-107">Det här kommandot accepterar en komprimerad fil som har fil namns tillägget. zip.</span><span class="sxs-lookup"><span data-stu-id="246c3-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="246c3-108">Filen innehåller en mapp som innehåller en fil som är en av följande typer:</span><span class="sxs-lookup"><span data-stu-id="246c3-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="246c3-109">Windows PowerShell-modul, som har fil namns tillägget. psm1 eller. dll</span><span class="sxs-lookup"><span data-stu-id="246c3-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="246c3-110">Manifestet för Windows PowerShell, som har fil namns tillägget. psd1 namnet på zip-filen, namnet på mappen och namnet på filen i mappen måste vara samma.</span><span class="sxs-lookup"><span data-stu-id="246c3-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="246c3-111">Ange zip-filen som en webb adress som Automation-tjänsten kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="246c3-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="246c3-112">Om du importerar en Windows PowerShell-modul till Automation med den här cmdleten eller Set-AzAutomationModule cmdlet är åtgärden asynkron.</span><span class="sxs-lookup"><span data-stu-id="246c3-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="246c3-113">Kommandot slutförs om importen lyckas eller inte.</span><span class="sxs-lookup"><span data-stu-id="246c3-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="246c3-114">Om du vill kontrol lera om det lyckades kör du följande kommando: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Modulnamn kontrol lera egenskapen **ProvisioningState** efter värdet lyckades.</span><span class="sxs-lookup"><span data-stu-id="246c3-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="246c3-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="246c3-115">EXAMPLES</span></span>

### <span data-ttu-id="246c3-116">Exempel 1: importera en modul</span><span class="sxs-lookup"><span data-stu-id="246c3-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="246c3-117">Det här kommandot importerar en modul som heter ContosoModule till det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="246c3-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="246c3-118">Modulen är lagrad i en Azure-blob i ett lagrings konto med namnet contosostorage och en container som heter modules.</span><span class="sxs-lookup"><span data-stu-id="246c3-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="246c3-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="246c3-119">PARAMETERS</span></span>

### <span data-ttu-id="246c3-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="246c3-120">-AutomationAccountName</span></span>
<span data-ttu-id="246c3-121">Anger namnet på det Automation-konto som denna cmdlet importerar en modul för.</span><span class="sxs-lookup"><span data-stu-id="246c3-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="246c3-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="246c3-122">-ContentLinkUri</span></span>
<span data-ttu-id="246c3-123">URL-adressen till ett zip-paket för en modul</span><span class="sxs-lookup"><span data-stu-id="246c3-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="246c3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246c3-124">-DefaultProfile</span></span>
<span data-ttu-id="246c3-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="246c3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="246c3-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="246c3-126">-Name</span></span>
<span data-ttu-id="246c3-127">Anger namnet på den modul som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="246c3-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="246c3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="246c3-128">-ResourceGroupName</span></span>
<span data-ttu-id="246c3-129">Anger namnet på en resurs grupp för vilken denna cmdlet importerar en modul.</span><span class="sxs-lookup"><span data-stu-id="246c3-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="246c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246c3-130">CommonParameters</span></span>
<span data-ttu-id="246c3-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="246c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246c3-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="246c3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246c3-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="246c3-133">INPUTS</span></span>

### <span data-ttu-id="246c3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="246c3-134">System.String</span></span>

### <span data-ttu-id="246c3-135">System. URI</span><span class="sxs-lookup"><span data-stu-id="246c3-135">System.Uri</span></span>

## <span data-ttu-id="246c3-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="246c3-136">OUTPUTS</span></span>

### <span data-ttu-id="246c3-137">Microsoft. Azure. commands. Automation. Model. modul</span><span class="sxs-lookup"><span data-stu-id="246c3-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="246c3-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="246c3-138">NOTES</span></span>

## <span data-ttu-id="246c3-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="246c3-139">RELATED LINKS</span></span>

[<span data-ttu-id="246c3-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="246c3-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="246c3-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="246c3-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="246c3-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="246c3-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


