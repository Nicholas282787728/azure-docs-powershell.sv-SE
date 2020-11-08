---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270314"
---
# <span data-ttu-id="31a76-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="31a76-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="31a76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31a76-102">SYNOPSIS</span></span>
<span data-ttu-id="31a76-103">Uppdaterar en modul i Automation.</span><span class="sxs-lookup"><span data-stu-id="31a76-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="31a76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31a76-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31a76-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31a76-105">DESCRIPTION</span></span>
<span data-ttu-id="31a76-106">Cmdleten **set-AzAutomationModule** uppdaterar en modul i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="31a76-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="31a76-107">Det här kommandot accepterar en komprimerad fil som har fil namns tillägget. zip.</span><span class="sxs-lookup"><span data-stu-id="31a76-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="31a76-108">Filen innehåller en mapp som innehåller en fil som är en av följande typer:</span><span class="sxs-lookup"><span data-stu-id="31a76-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="31a76-109">wps_2 modul, som har fil namns tillägget. psm1 eller. dll</span><span class="sxs-lookup"><span data-stu-id="31a76-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="31a76-110">wps_2 modul manifest, som har fil namns tillägget. psd1 namnet på zip-filen, namnet på mappen och namnet på filen i mappen måste vara samma.</span><span class="sxs-lookup"><span data-stu-id="31a76-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="31a76-111">Ange zip-filen som en webb adress som Automation-tjänsten kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="31a76-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="31a76-112">Om du importerar en wps_2 modul till Automation med denna cmdlet eller New-AzAutomationModule cmdlet är åtgärden asynkron.</span><span class="sxs-lookup"><span data-stu-id="31a76-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="31a76-113">Kommandot slutförs om importen lyckas eller inte.</span><span class="sxs-lookup"><span data-stu-id="31a76-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="31a76-114">Om du vill kontrol lera om det lyckades kör du följande kommando: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Modulnamn kontrol lera egenskapen **ProvisioningState** efter värdet lyckades.</span><span class="sxs-lookup"><span data-stu-id="31a76-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="31a76-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31a76-115">EXAMPLES</span></span>

### <span data-ttu-id="31a76-116">Exempel 1: uppdatera en modul</span><span class="sxs-lookup"><span data-stu-id="31a76-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="31a76-117">Det här kommandot importerar en uppdaterad version av en befintlig modul som heter ContosoModule till Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="31a76-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="31a76-118">Modulen är lagrad i en Azure-blob i ett lagrings konto med namnet contosostorage och en container som heter modules.</span><span class="sxs-lookup"><span data-stu-id="31a76-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="31a76-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31a76-119">PARAMETERS</span></span>

### <span data-ttu-id="31a76-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="31a76-120">-AutomationAccountName</span></span>
<span data-ttu-id="31a76-121">Anger namnet på det Automation-konto som denna cmdlet uppdaterar en modul för.</span><span class="sxs-lookup"><span data-stu-id="31a76-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="31a76-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="31a76-122">-ContentLinkUri</span></span>
<span data-ttu-id="31a76-123">Anger URL-adressen till zip-filen som innehåller den nya versionen av en modul som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="31a76-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a76-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="31a76-124">-ContentLinkVersion</span></span>
<span data-ttu-id="31a76-125">Anger vilken version av modulen som den här cmdleten uppdaterar Automation.</span><span class="sxs-lookup"><span data-stu-id="31a76-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a76-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a76-126">-DefaultProfile</span></span>
<span data-ttu-id="31a76-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="31a76-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31a76-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="31a76-128">-Name</span></span>
<span data-ttu-id="31a76-129">Anger namnet på den modul som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="31a76-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="31a76-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a76-130">-ResourceGroupName</span></span>
<span data-ttu-id="31a76-131">Anger namnet på en resurs grupp som denna cmdlet uppdaterar en modul för.</span><span class="sxs-lookup"><span data-stu-id="31a76-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="31a76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a76-132">CommonParameters</span></span>
<span data-ttu-id="31a76-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a76-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a76-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a76-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31a76-135">INPUTS</span></span>

### <span data-ttu-id="31a76-136">System. String</span><span class="sxs-lookup"><span data-stu-id="31a76-136">System.String</span></span>

### <span data-ttu-id="31a76-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="31a76-137">System.Uri</span></span>

## <span data-ttu-id="31a76-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31a76-138">OUTPUTS</span></span>

### <span data-ttu-id="31a76-139">Microsoft. Azure. commands. Automation. Model. modul</span><span class="sxs-lookup"><span data-stu-id="31a76-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="31a76-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31a76-140">NOTES</span></span>

## <span data-ttu-id="31a76-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31a76-141">RELATED LINKS</span></span>

[<span data-ttu-id="31a76-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="31a76-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="31a76-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="31a76-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="31a76-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="31a76-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


