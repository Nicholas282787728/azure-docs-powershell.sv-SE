---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 0ff9ef1337a1f2a5f0503c59dc4e6240d3c959b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101110"
---
# <span data-ttu-id="09d45-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="09d45-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="09d45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09d45-102">SYNOPSIS</span></span>
<span data-ttu-id="09d45-103">Kryptera Credential i den länkade tjänsten med den angivna integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="09d45-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="09d45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09d45-104">SYNTAX</span></span>

### <span data-ttu-id="09d45-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="09d45-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d45-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="09d45-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09d45-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09d45-107">DESCRIPTION</span></span>
<span data-ttu-id="09d45-108">New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet krypterar autentiseringsuppgiften i den länkade tjänsten med den angivna integrerings körnings miljön.</span><span class="sxs-lookup"><span data-stu-id="09d45-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="09d45-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09d45-109">EXAMPLES</span></span>

### <span data-ttu-id="09d45-110">Exempel 1: kryptera autentiseringsuppgifter i en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="09d45-110">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="09d45-111">Det här kommandot krypterar autentiseringsuppgifter i filen C:\samples\WikiSample\TaxiDemo1.jspå med integrerings körningen tested-selfhost-IR.</span><span class="sxs-lookup"><span data-stu-id="09d45-111">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="09d45-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09d45-112">PARAMETERS</span></span>

### <span data-ttu-id="09d45-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="09d45-113">-DataFactory</span></span>
<span data-ttu-id="09d45-114">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="09d45-114">The data factory object.</span></span>

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

### <span data-ttu-id="09d45-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="09d45-115">-DataFactoryName</span></span>
<span data-ttu-id="09d45-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="09d45-116">The data factory name.</span></span>

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

### <span data-ttu-id="09d45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d45-117">-DefaultProfile</span></span>
<span data-ttu-id="09d45-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09d45-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09d45-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="09d45-119">-DefinitionFile</span></span>
<span data-ttu-id="09d45-120">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="09d45-120">The JSON file path.</span></span>

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

### <span data-ttu-id="09d45-121">-Force</span><span class="sxs-lookup"><span data-stu-id="09d45-121">-Force</span></span>
<span data-ttu-id="09d45-122">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="09d45-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="09d45-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="09d45-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="09d45-124">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="09d45-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="09d45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d45-125">-ResourceGroupName</span></span>
<span data-ttu-id="09d45-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="09d45-126">The resource group name.</span></span>

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

### <span data-ttu-id="09d45-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09d45-127">-Confirm</span></span>
<span data-ttu-id="09d45-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09d45-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09d45-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09d45-129">-WhatIf</span></span>
<span data-ttu-id="09d45-130">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09d45-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="09d45-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d45-131">CommonParameters</span></span>
<span data-ttu-id="09d45-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09d45-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d45-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09d45-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d45-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09d45-134">INPUTS</span></span>

### <span data-ttu-id="09d45-135">System. String</span><span class="sxs-lookup"><span data-stu-id="09d45-135">System.String</span></span>

### <span data-ttu-id="09d45-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="09d45-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="09d45-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09d45-137">OUTPUTS</span></span>

### <span data-ttu-id="09d45-138">System. String</span><span class="sxs-lookup"><span data-stu-id="09d45-138">System.String</span></span>

## <span data-ttu-id="09d45-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09d45-139">NOTES</span></span>

## <span data-ttu-id="09d45-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09d45-140">RELATED LINKS</span></span>
