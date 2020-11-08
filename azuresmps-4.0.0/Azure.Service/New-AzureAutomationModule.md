---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099453"
---
# <span data-ttu-id="d8da0-101">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d8da0-101">New-AzureAutomationModule</span></span>

## <span data-ttu-id="d8da0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8da0-102">SYNOPSIS</span></span>

<span data-ttu-id="d8da0-103">Importerar en modul till Automation.</span><span class="sxs-lookup"><span data-stu-id="d8da0-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="d8da0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8da0-104">SYNTAX</span></span>

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d8da0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8da0-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="d8da0-106">Cmdleten **New-AzureAutomationModule** importerar en modul till Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d8da0-106">The **New-AzureAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="d8da0-107">En modul är en komprimerad fil med fil tillägget. zip som innehåller en mapp som innehåller någon av följande filtyper:</span><span class="sxs-lookup"><span data-stu-id="d8da0-107">A module is a compressed file, with a .zip extension, that contains a folder which includes one of the following file types:</span></span>

- <span data-ttu-id="d8da0-108">En Windows PowerShell-modul (psm1-fil).</span><span class="sxs-lookup"><span data-stu-id="d8da0-108">A Windows PowerShell module (psm1 file).</span></span> 

- <span data-ttu-id="d8da0-109">Ett manifest för Windows PowerShell-modulen (psd1-fil).</span><span class="sxs-lookup"><span data-stu-id="d8da0-109">A Windows PowerShell module manifest (psd1 file).</span></span> 

- <span data-ttu-id="d8da0-110">En sammansättning (DLL-fil).</span><span class="sxs-lookup"><span data-stu-id="d8da0-110">An assembly (dll file).</span></span>

<span data-ttu-id="d8da0-111">Namnen på zip-filen, mappen i zip-filen och filen i mappen (. psm1, PSD. 1 eller. dll) måste stämma överens.</span><span class="sxs-lookup"><span data-stu-id="d8da0-111">The names of the zip file, the folder in the zip file, and file in the folder (.psm1, psd.1, or .dll) must match.</span></span>

## <span data-ttu-id="d8da0-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8da0-112">EXAMPLES</span></span>

### <span data-ttu-id="d8da0-113">Exempel 1: importera en modul</span><span class="sxs-lookup"><span data-stu-id="d8da0-113">Example 1: Import a module</span></span>
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

<span data-ttu-id="d8da0-114">Det här kommandot importerar en modul som heter ContosoModule till det Automation-konto som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d8da0-114">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="d8da0-115">Modulen är lagrad i en Azure-blob i ett lagrings konto med namnet contosostorage och en container som heter modules.</span><span class="sxs-lookup"><span data-stu-id="d8da0-115">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="d8da0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8da0-116">PARAMETERS</span></span>

### <span data-ttu-id="d8da0-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8da0-117">-AutomationAccountName</span></span>
<span data-ttu-id="d8da0-118">Anger namnet på Automation-kontot som modulen lagras i.</span><span class="sxs-lookup"><span data-stu-id="d8da0-118">Specifies the name of the Automation account the module will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8da0-119">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="d8da0-119">-ContentLink</span></span>
<span data-ttu-id="d8da0-120">Offentlig URL, till exempel en webbplats eller en Azure-blob som anger sökvägen till filen.</span><span class="sxs-lookup"><span data-stu-id="d8da0-120">Public URL such as a website or Azure blob storage specifying the path to the module file.</span></span>
<span data-ttu-id="d8da0-121">Denna plats måste vara offentligt tillgänglig.</span><span class="sxs-lookup"><span data-stu-id="d8da0-121">This location must be publically accessible.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8da0-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8da0-122">-Name</span></span>
<span data-ttu-id="d8da0-123">Anger ett namn för modulen.</span><span class="sxs-lookup"><span data-stu-id="d8da0-123">Specifies a name for the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8da0-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8da0-124">-Profile</span></span>
<span data-ttu-id="d8da0-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d8da0-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8da0-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d8da0-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8da0-127">-Taggar</span><span class="sxs-lookup"><span data-stu-id="d8da0-127">-Tags</span></span>
<span data-ttu-id="d8da0-128">Anger en eller flera taggar som är relaterade till modulen.</span><span class="sxs-lookup"><span data-stu-id="d8da0-128">Specifies one or more tags related to the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8da0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8da0-129">CommonParameters</span></span>
<span data-ttu-id="d8da0-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8da0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8da0-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8da0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8da0-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8da0-132">INPUTS</span></span>

## <span data-ttu-id="d8da0-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8da0-133">OUTPUTS</span></span>

### <span data-ttu-id="d8da0-134">Microsoft. Azure. commands. Automation. Model. modul</span><span class="sxs-lookup"><span data-stu-id="d8da0-134">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="d8da0-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8da0-135">NOTES</span></span>

## <span data-ttu-id="d8da0-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8da0-136">RELATED LINKS</span></span>

[<span data-ttu-id="d8da0-137">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d8da0-137">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="d8da0-138">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d8da0-138">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="d8da0-139">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d8da0-139">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


