---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425672"
---
# <span data-ttu-id="bd011-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="bd011-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="bd011-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd011-102">SYNOPSIS</span></span>
<span data-ttu-id="bd011-103">Exporterar webb tjänst definitions objekt som en JSON-formaterad sträng.</span><span class="sxs-lookup"><span data-stu-id="bd011-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="bd011-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd011-104">SYNTAX</span></span>

### <span data-ttu-id="bd011-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="bd011-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd011-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="bd011-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd011-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd011-107">DESCRIPTION</span></span>
<span data-ttu-id="bd011-108">Exporterar definitionsfiler för den angivna webb tjänsten som en JSON-formaterad sträng.</span><span class="sxs-lookup"><span data-stu-id="bd011-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="bd011-109">Du kan returnera strängen direkt eller spara den i en fil.</span><span class="sxs-lookup"><span data-stu-id="bd011-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="bd011-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd011-110">EXAMPLES</span></span>

### <span data-ttu-id="bd011-111">Exempel 1: exportera som sträng</span><span class="sxs-lookup"><span data-stu-id="bd011-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="bd011-112">Exempel 2: exportera till filen</span><span class="sxs-lookup"><span data-stu-id="bd011-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="bd011-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd011-113">PARAMETERS</span></span>

### <span data-ttu-id="bd011-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd011-114">-DefaultProfile</span></span>
<span data-ttu-id="bd011-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bd011-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd011-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bd011-116">-Force</span></span>
<span data-ttu-id="bd011-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bd011-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd011-118">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="bd011-118">-OutputFile</span></span>
<span data-ttu-id="bd011-119">Sökvägen till den exporterade definitionen.</span><span class="sxs-lookup"><span data-stu-id="bd011-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd011-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="bd011-120">-ToJsonString</span></span>
<span data-ttu-id="bd011-121">Anger att definitionen exporteras som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="bd011-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd011-122">-Webservice</span><span class="sxs-lookup"><span data-stu-id="bd011-122">-WebService</span></span>
<span data-ttu-id="bd011-123">Webb tjänst definitions objekt som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="bd011-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd011-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd011-124">-Confirm</span></span>
<span data-ttu-id="bd011-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd011-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd011-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd011-126">-WhatIf</span></span>
<span data-ttu-id="bd011-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd011-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd011-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd011-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd011-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd011-129">CommonParameters</span></span>
<span data-ttu-id="bd011-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd011-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd011-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd011-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd011-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd011-132">INPUTS</span></span>

### <span data-ttu-id="bd011-133">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="bd011-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="bd011-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd011-134">OUTPUTS</span></span>

### <span data-ttu-id="bd011-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bd011-135">System.String</span></span>

## <span data-ttu-id="bd011-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd011-136">NOTES</span></span>
<span data-ttu-id="bd011-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="bd011-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="bd011-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd011-138">RELATED LINKS</span></span>
