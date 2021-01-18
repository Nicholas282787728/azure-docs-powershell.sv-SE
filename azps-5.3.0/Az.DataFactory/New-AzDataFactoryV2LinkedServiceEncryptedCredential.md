---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: a99f7fbb1383d685a53cc11f9dd81f6f306ed633
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524178"
---
# <span data-ttu-id="8494b-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="8494b-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="8494b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8494b-102">SYNOPSIS</span></span>
<span data-ttu-id="8494b-103">Kryptera Credential i den länkade tjänsten med den angivna integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="8494b-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="8494b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8494b-104">SYNTAX</span></span>

### <span data-ttu-id="8494b-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="8494b-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8494b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8494b-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8494b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8494b-107">DESCRIPTION</span></span>
<span data-ttu-id="8494b-108">New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet krypterar autentiseringsuppgiften i den länkade tjänsten med den angivna integrerings körnings miljön.</span><span class="sxs-lookup"><span data-stu-id="8494b-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="8494b-109">Se till att följande förutsättningar uppfylls:</span><span class="sxs-lookup"><span data-stu-id="8494b-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="8494b-110">Alternativet **fjärråtkomst** är aktiverat i den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="8494b-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="8494b-111">PowerShell 7,0 eller senare används för att köra cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8494b-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="8494b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8494b-112">EXAMPLES</span></span>

### <span data-ttu-id="8494b-113">Exempel 1: kryptera autentiseringsuppgifter i en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="8494b-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="8494b-114">Det här kommandot krypterar autentiseringsuppgifter i filen C:\samples\WikiSample\TaxiDemo1.jspå med integrerings körningen tested-selfhost-IR.</span><span class="sxs-lookup"><span data-stu-id="8494b-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="8494b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8494b-115">PARAMETERS</span></span>

### <span data-ttu-id="8494b-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8494b-116">-DataFactory</span></span>
<span data-ttu-id="8494b-117">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="8494b-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8494b-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8494b-118">-DataFactoryName</span></span>
<span data-ttu-id="8494b-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="8494b-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8494b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8494b-120">-DefaultProfile</span></span>
<span data-ttu-id="8494b-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8494b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8494b-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="8494b-122">-DefinitionFile</span></span>
<span data-ttu-id="8494b-123">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="8494b-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8494b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8494b-124">-Force</span></span>
<span data-ttu-id="8494b-125">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8494b-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8494b-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8494b-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8494b-127">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="8494b-127">The integration runtime name.</span></span>

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

### <span data-ttu-id="8494b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8494b-128">-ResourceGroupName</span></span>
<span data-ttu-id="8494b-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8494b-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8494b-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8494b-130">-Confirm</span></span>
<span data-ttu-id="8494b-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8494b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8494b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8494b-132">-WhatIf</span></span>
<span data-ttu-id="8494b-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8494b-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8494b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8494b-134">CommonParameters</span></span>
<span data-ttu-id="8494b-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8494b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8494b-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8494b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8494b-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8494b-137">INPUTS</span></span>

### <span data-ttu-id="8494b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8494b-138">System.String</span></span>

### <span data-ttu-id="8494b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8494b-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8494b-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8494b-140">OUTPUTS</span></span>

### <span data-ttu-id="8494b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8494b-141">System.String</span></span>

## <span data-ttu-id="8494b-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8494b-142">NOTES</span></span>

## <span data-ttu-id="8494b-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8494b-143">RELATED LINKS</span></span>
