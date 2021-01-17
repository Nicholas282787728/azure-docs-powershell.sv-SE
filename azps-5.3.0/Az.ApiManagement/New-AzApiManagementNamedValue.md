---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementNamedValue.md
ms.openlocfilehash: 08e29c91e253c648b774e56d7e236accdd5fbff0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423640"
---
# <span data-ttu-id="9926a-101">New-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="9926a-101">New-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="9926a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9926a-102">SYNOPSIS</span></span>
<span data-ttu-id="9926a-103">Skapar ett nytt namngivet värde.</span><span class="sxs-lookup"><span data-stu-id="9926a-103">Creates new Named Value.</span></span>

## <span data-ttu-id="9926a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9926a-104">SYNTAX</span></span>

```
New-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9926a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9926a-105">DESCRIPTION</span></span>
<span data-ttu-id="9926a-106">Cmdleten **New-AzApiManagementNamedValue** skapar ett **värde** för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="9926a-106">The **New-AzApiManagementNamedValue** cmdlet creates an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="9926a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9926a-107">EXAMPLES</span></span>

### <span data-ttu-id="9926a-108">Exempel 1: skapa ett namngivet värde som innehåller Taggar</span><span class="sxs-lookup"><span data-stu-id="9926a-108">Example 1: Create a named value that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="9926a-109">Det första kommandot tilldelar två värden till $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="9926a-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="9926a-110">Det andra kommandot skapar ett namngivet värde och tilldelar strängarna i $Tags som taggar på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="9926a-110">The second command creates a named value and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="9926a-111">Exempel 2: skapa ett namngivet värde med ett hemligt värde</span><span class="sxs-lookup"><span data-stu-id="9926a-111">Example 2: Create a named value that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="9926a-112">Det här kommandot skapar ett **namngivet värde** som har ett krypterat värde.</span><span class="sxs-lookup"><span data-stu-id="9926a-112">This command creates a **Named Value** that has a value that is encrypted.</span></span>

## <span data-ttu-id="9926a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9926a-113">PARAMETERS</span></span>

### <span data-ttu-id="9926a-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9926a-114">-Context</span></span>
<span data-ttu-id="9926a-115">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9926a-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9926a-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9926a-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9926a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9926a-117">-DefaultProfile</span></span>
<span data-ttu-id="9926a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9926a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9926a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="9926a-119">-Name</span></span>
<span data-ttu-id="9926a-120">Namnet på det namngivna värdet.</span><span class="sxs-lookup"><span data-stu-id="9926a-120">Name of the named value.</span></span>
<span data-ttu-id="9926a-121">Maximal längd är 100 tecken.</span><span class="sxs-lookup"><span data-stu-id="9926a-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="9926a-122">Det får bara innehålla bokstäver, siffror, punkter, streck och under streck.</span><span class="sxs-lookup"><span data-stu-id="9926a-122">It may contain only letters, digits, period, dash, and underscore characters.</span></span>
<span data-ttu-id="9926a-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9926a-123">This parameter is required.</span></span>

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

### <span data-ttu-id="9926a-124">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="9926a-124">-NamedValueId</span></span>
<span data-ttu-id="9926a-125">Identifierare för det nya namngivna värdet.</span><span class="sxs-lookup"><span data-stu-id="9926a-125">Identifier of new named value.</span></span>
<span data-ttu-id="9926a-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9926a-126">This parameter is optional.</span></span>
<span data-ttu-id="9926a-127">Om det inte anges kommer att genereras.</span><span class="sxs-lookup"><span data-stu-id="9926a-127">If not specified will be generated.</span></span>

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

### <span data-ttu-id="9926a-128">-Secret</span><span class="sxs-lookup"><span data-stu-id="9926a-128">-Secret</span></span>
<span data-ttu-id="9926a-129">Avgör om värdet är hemligt och ska vara krypterat eller inte.</span><span class="sxs-lookup"><span data-stu-id="9926a-129">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="9926a-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9926a-130">This parameter is optional.</span></span>
<span data-ttu-id="9926a-131">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="9926a-131">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926a-132">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9926a-132">-Tag</span></span>
<span data-ttu-id="9926a-133">Taggar som ska kopplas till det namngivna värdet.</span><span class="sxs-lookup"><span data-stu-id="9926a-133">Tags to be associated with named value.</span></span>
<span data-ttu-id="9926a-134">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="9926a-134">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9926a-135">-Värde</span><span class="sxs-lookup"><span data-stu-id="9926a-135">-Value</span></span>
<span data-ttu-id="9926a-136">Värdet för det namngivna värdet.</span><span class="sxs-lookup"><span data-stu-id="9926a-136">Value of the named value.</span></span>
<span data-ttu-id="9926a-137">Kan innehålla princip uttryck.</span><span class="sxs-lookup"><span data-stu-id="9926a-137">Can contain policy expressions.</span></span>
<span data-ttu-id="9926a-138">Maximal längd är 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="9926a-138">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="9926a-139">Den får inte vara tom eller bestå bara av blank steg.</span><span class="sxs-lookup"><span data-stu-id="9926a-139">It may not be empty or consist only of whitespace.</span></span>
<span data-ttu-id="9926a-140">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="9926a-140">This parameter is required.</span></span>

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

### <span data-ttu-id="9926a-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9926a-141">-Confirm</span></span>
<span data-ttu-id="9926a-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9926a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9926a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9926a-143">-WhatIf</span></span>
<span data-ttu-id="9926a-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9926a-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9926a-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9926a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9926a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9926a-146">CommonParameters</span></span>
<span data-ttu-id="9926a-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9926a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9926a-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9926a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9926a-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9926a-149">INPUTS</span></span>

### <span data-ttu-id="9926a-150">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9926a-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9926a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="9926a-151">System.String</span></span>

### <span data-ttu-id="9926a-152">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9926a-152">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9926a-153">System. string []</span><span class="sxs-lookup"><span data-stu-id="9926a-153">System.String[]</span></span>

## <span data-ttu-id="9926a-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9926a-154">OUTPUTS</span></span>

### <span data-ttu-id="9926a-155">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="9926a-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="9926a-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9926a-156">NOTES</span></span>

## <span data-ttu-id="9926a-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9926a-157">RELATED LINKS</span></span>
