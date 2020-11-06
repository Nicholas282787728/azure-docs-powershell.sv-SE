---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: e2de3546f805e006bd7f48e2ee7f95b8f3347544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586252"
---
# <span data-ttu-id="29187-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="29187-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="29187-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29187-102">SYNOPSIS</span></span>
<span data-ttu-id="29187-103">Importerar en modul till Automation.</span><span class="sxs-lookup"><span data-stu-id="29187-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29187-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29187-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> -ContentLinkUri <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29187-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29187-105">DESCRIPTION</span></span>
<span data-ttu-id="29187-106">Cmdleten **New-AzureRmAutomationModule** importerar en modul till Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="29187-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="29187-107">Det här kommandot accepterar en komprimerad fil som har fil namns tillägget. zip.</span><span class="sxs-lookup"><span data-stu-id="29187-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="29187-108">Filen innehåller en mapp som innehåller en fil som är en av följande typer:</span><span class="sxs-lookup"><span data-stu-id="29187-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="29187-109">wps_2 modul, som har fil namns tillägget. psm1 eller. dll</span><span class="sxs-lookup"><span data-stu-id="29187-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="29187-110">wps_2 modul manifest, som har fil namns tillägget. psd1</span><span class="sxs-lookup"><span data-stu-id="29187-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="29187-111">Namnet på zip-filen, namnet på mappen och namnet på filen i mappen måste vara samma.</span><span class="sxs-lookup"><span data-stu-id="29187-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="29187-112">Ange zip-filen som en webb adress som Automation-tjänsten kan komma åt.</span><span class="sxs-lookup"><span data-stu-id="29187-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="29187-113">Om du importerar en wps_2 modul till Automation med denna cmdlet eller Set-AzureRmAutomationModule cmdlet är åtgärden asynkron.</span><span class="sxs-lookup"><span data-stu-id="29187-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="29187-114">Kommandot slutförs om importen lyckas eller inte.</span><span class="sxs-lookup"><span data-stu-id="29187-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="29187-115">Om du vill kontrol lera om det lyckades kör du följande kommando:</span><span class="sxs-lookup"><span data-stu-id="29187-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="29187-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `Modulnamn</span><span class="sxs-lookup"><span data-stu-id="29187-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="29187-117">Kontrol lera värdet slutfört med egenskapen **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="29187-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="29187-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29187-118">EXAMPLES</span></span>

### <span data-ttu-id="29187-119">Exempel 1: importera en modul</span><span class="sxs-lookup"><span data-stu-id="29187-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="29187-120">Det här kommandot importerar en modul som heter ContosoModule till det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="29187-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="29187-121">Modulen är lagrad i en Azure-blob i ett lagrings konto med namnet contosostorage och en container som heter modules.</span><span class="sxs-lookup"><span data-stu-id="29187-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="29187-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29187-122">PARAMETERS</span></span>

### <span data-ttu-id="29187-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="29187-123">-AutomationAccountName</span></span>
<span data-ttu-id="29187-124">Anger namnet på det Automation-konto som denna cmdlet importerar en modul för.</span><span class="sxs-lookup"><span data-stu-id="29187-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="29187-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="29187-125">-ContentLinkUri</span></span>
<span data-ttu-id="29187-126">URL-adressen till ett zip-paket för en modul.</span><span class="sxs-lookup"><span data-stu-id="29187-126">The url to a module zip package.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29187-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="29187-127">-Name</span></span>
<span data-ttu-id="29187-128">Anger namnet på den modul som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="29187-128">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="29187-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29187-129">-ResourceGroupName</span></span>
<span data-ttu-id="29187-130">Anger namnet på en resurs grupp för vilken denna cmdlet importerar en modul.</span><span class="sxs-lookup"><span data-stu-id="29187-130">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="29187-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29187-131">-DefaultProfile</span></span>
<span data-ttu-id="29187-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29187-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29187-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29187-133">CommonParameters</span></span>
<span data-ttu-id="29187-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29187-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29187-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29187-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29187-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29187-136">INPUTS</span></span>

## <span data-ttu-id="29187-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29187-137">OUTPUTS</span></span>

### <span data-ttu-id="29187-138">Microsoft. Azure. commands. Automation. Model. modul</span><span class="sxs-lookup"><span data-stu-id="29187-138">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="29187-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29187-139">NOTES</span></span>

## <span data-ttu-id="29187-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29187-140">RELATED LINKS</span></span>

[<span data-ttu-id="29187-141">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="29187-141">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="29187-142">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="29187-142">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="29187-143">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="29187-143">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


