---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: fd07ab55fad93fdf48df52e15db846630ba6c1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584320"
---
# <span data-ttu-id="3ffce-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="3ffce-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="3ffce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ffce-102">SYNOPSIS</span></span>
<span data-ttu-id="3ffce-103">Exporterar webb tjänst definitions objekt som en JSON-formaterad sträng.</span><span class="sxs-lookup"><span data-stu-id="3ffce-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ffce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ffce-104">SYNTAX</span></span>

### <span data-ttu-id="3ffce-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="3ffce-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ffce-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="3ffce-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ffce-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ffce-107">DESCRIPTION</span></span>
<span data-ttu-id="3ffce-108">Exporterar definitionsfiler för den angivna webb serving som en JSON-formaterad sträng.</span><span class="sxs-lookup"><span data-stu-id="3ffce-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="3ffce-109">Du kan returnera strängen direkt eller spara den i en fil.</span><span class="sxs-lookup"><span data-stu-id="3ffce-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="3ffce-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ffce-110">EXAMPLES</span></span>

### <span data-ttu-id="3ffce-111">--------------------------Exempel 1: exportera som sträng--------------------------</span><span class="sxs-lookup"><span data-stu-id="3ffce-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="3ffce-112">--------------------------Exempel 2: exportera till fil--------------------------</span><span class="sxs-lookup"><span data-stu-id="3ffce-112">--------------------------  Example 2: Export to file  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="3ffce-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ffce-113">PARAMETERS</span></span>

### <span data-ttu-id="3ffce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ffce-114">-DefaultProfile</span></span>
<span data-ttu-id="3ffce-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3ffce-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffce-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3ffce-116">-Force</span></span>
<span data-ttu-id="3ffce-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3ffce-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffce-118">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="3ffce-118">-OutputFile</span></span>
<span data-ttu-id="3ffce-119">Sökvägen till den exporterade definitionen.</span><span class="sxs-lookup"><span data-stu-id="3ffce-119">The file path for exported definition.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffce-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="3ffce-120">-ToJsonString</span></span>
<span data-ttu-id="3ffce-121">Anger att definitionen exporteras som en JSON-sträng.</span><span class="sxs-lookup"><span data-stu-id="3ffce-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToJSON
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffce-122">-Webservice</span><span class="sxs-lookup"><span data-stu-id="3ffce-122">-WebService</span></span>
<span data-ttu-id="3ffce-123">Webb tjänst definitions objekt som ska exporteras.</span><span class="sxs-lookup"><span data-stu-id="3ffce-123">The web service definition object to be exported.</span></span>

```yaml
Type: WebService
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ffce-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ffce-124">-Confirm</span></span>
<span data-ttu-id="3ffce-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ffce-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ffce-126">-WhatIf</span></span>
<span data-ttu-id="3ffce-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3ffce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ffce-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3ffce-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ffce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ffce-129">CommonParameters</span></span>
<span data-ttu-id="3ffce-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ffce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ffce-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ffce-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ffce-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ffce-132">INPUTS</span></span>

### <span data-ttu-id="3ffce-133">Webb tjänst</span><span class="sxs-lookup"><span data-stu-id="3ffce-133">WebService</span></span>
<span data-ttu-id="3ffce-134">Parametern "WebService" accepterar värdet för typen "WebService" från pipeline</span><span class="sxs-lookup"><span data-stu-id="3ffce-134">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="3ffce-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ffce-135">OUTPUTS</span></span>

### <span data-ttu-id="3ffce-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="3ffce-136">None</span></span>

## <span data-ttu-id="3ffce-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ffce-137">NOTES</span></span>
<span data-ttu-id="3ffce-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="3ffce-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3ffce-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ffce-139">RELATED LINKS</span></span>

