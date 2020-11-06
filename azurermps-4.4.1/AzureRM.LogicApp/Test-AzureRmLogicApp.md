---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: fa848a8249fa01a61a7aa50855f24b2813b9fdf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586483"
---
# <span data-ttu-id="a638e-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a638e-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="a638e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a638e-102">SYNOPSIS</span></span>
<span data-ttu-id="a638e-103">Validerar en logik program definition.</span><span class="sxs-lookup"><span data-stu-id="a638e-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a638e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a638e-104">SYNTAX</span></span>

### <span data-ttu-id="a638e-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a638e-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a638e-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a638e-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a638e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a638e-107">DESCRIPTION</span></span>
<span data-ttu-id="a638e-108">**Test-AzureRmLogicApp** cmdlet verifierar en logik program definition i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a638e-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="a638e-109">Ange namnet på logik programmet, resurs gruppens namn, plats, delstat, integrerings konto-ID eller parametrar.</span><span class="sxs-lookup"><span data-stu-id="a638e-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>

<span data-ttu-id="a638e-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="a638e-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a638e-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="a638e-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a638e-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="a638e-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a638e-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="a638e-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a638e-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a638e-114">EXAMPLES</span></span>

### <span data-ttu-id="a638e-115">Exempel 1: validera en logik-app genom att använda fil Sök vägar</span><span class="sxs-lookup"><span data-stu-id="a638e-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="a638e-116">Det här kommandot verifierar en logik-app som heter LogicApp01 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a638e-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="a638e-117">Kommandot anger sökväg för definiering och parameter fil.</span><span class="sxs-lookup"><span data-stu-id="a638e-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="a638e-118">Exempel 2: validera ett logiskt program med hjälp av objekt</span><span class="sxs-lookup"><span data-stu-id="a638e-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="a638e-119">Det här kommandot verifierar en logik-app som heter LogicApp01 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a638e-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="a638e-120">Kommandot anger definitioner och parameter objekt.</span><span class="sxs-lookup"><span data-stu-id="a638e-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="a638e-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a638e-121">PARAMETERS</span></span>

### <span data-ttu-id="a638e-122">-Definition</span><span class="sxs-lookup"><span data-stu-id="a638e-122">-Definition</span></span>
<span data-ttu-id="a638e-123">Anger definitionen för en logik-app som ett objekt eller en sträng i JSON-format (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="a638e-123">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a638e-124">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="a638e-124">-DefinitionFilePath</span></span>
<span data-ttu-id="a638e-125">Anger definitionen för din logik-app som sökväg till en definitions fil i JSON-format.</span><span class="sxs-lookup"><span data-stu-id="a638e-125">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a638e-126">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="a638e-126">-IntegrationAccountId</span></span>
<span data-ttu-id="a638e-127">Anger ett integrerings konto-ID för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="a638e-127">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a638e-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="a638e-128">-Location</span></span>
<span data-ttu-id="a638e-129">Anger platsen för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="a638e-129">Specifies the location of the logic app.</span></span>
<span data-ttu-id="a638e-130">Ange en plats för Azure Data Center, till exempel West US eller Sydostasien.</span><span class="sxs-lookup"><span data-stu-id="a638e-130">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="a638e-131">Du kan placera ett logiskt program på valfri plats.</span><span class="sxs-lookup"><span data-stu-id="a638e-131">You can place a logic app in any location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a638e-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="a638e-132">-Name</span></span>
<span data-ttu-id="a638e-133">Anger namnet på logik programmet.</span><span class="sxs-lookup"><span data-stu-id="a638e-133">Specifies the name of the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a638e-134">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="a638e-134">-ParameterFilePath</span></span>
<span data-ttu-id="a638e-135">Anger sökvägen till en JSON-formaterad parameter fil.</span><span class="sxs-lookup"><span data-stu-id="a638e-135">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a638e-136">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="a638e-136">-Parameters</span></span>
<span data-ttu-id="a638e-137">Anger ett samlings objekt i logik programmet.</span><span class="sxs-lookup"><span data-stu-id="a638e-137">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="a638e-138">Ange en hash-tabell, en ord lista \<string\> eller en ord lista \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="a638e-138">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a638e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a638e-139">-ResourceGroupName</span></span>
<span data-ttu-id="a638e-140">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a638e-140">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a638e-141">-State</span><span class="sxs-lookup"><span data-stu-id="a638e-141">-State</span></span>
<span data-ttu-id="a638e-142">Anger ett tillstånd för logik programmet.</span><span class="sxs-lookup"><span data-stu-id="a638e-142">Specifies a state of the logic app.</span></span>
<span data-ttu-id="a638e-143">De acceptabla värdena för den här parametern är: Enabled och disabled.</span><span class="sxs-lookup"><span data-stu-id="a638e-143">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a638e-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a638e-144">-DefaultProfile</span></span>
<span data-ttu-id="a638e-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a638e-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a638e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a638e-146">CommonParameters</span></span>
<span data-ttu-id="a638e-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a638e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a638e-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a638e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a638e-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a638e-149">INPUTS</span></span>

## <span data-ttu-id="a638e-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a638e-150">OUTPUTS</span></span>

### <span data-ttu-id="a638e-151">System. Object</span><span class="sxs-lookup"><span data-stu-id="a638e-151">System.Object</span></span>

## <span data-ttu-id="a638e-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a638e-152">NOTES</span></span>

## <span data-ttu-id="a638e-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a638e-153">RELATED LINKS</span></span>

[<span data-ttu-id="a638e-154">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a638e-154">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="a638e-155">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a638e-155">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="a638e-156">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a638e-156">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="a638e-157">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a638e-157">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="a638e-158">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a638e-158">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


