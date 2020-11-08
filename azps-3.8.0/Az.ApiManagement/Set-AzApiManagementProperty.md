---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: 38c937de07d4a19a6c2632356c2b9ac58b2b416a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091896"
---
# <span data-ttu-id="6f947-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6f947-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="6f947-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f947-102">SYNOPSIS</span></span>
<span data-ttu-id="6f947-103">Ändrar en API-egenskap.</span><span class="sxs-lookup"><span data-stu-id="6f947-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="6f947-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f947-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f947-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f947-105">DESCRIPTION</span></span>
<span data-ttu-id="6f947-106">Cmdleten **set-AzApiManagementProperty** ändrar en egenskap för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="6f947-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="6f947-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f947-107">EXAMPLES</span></span>

### <span data-ttu-id="6f947-108">Exempel 1: ändra taggarna för en egenskap</span><span class="sxs-lookup"><span data-stu-id="6f947-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="6f947-109">Det första kommandot tilldelar två värden till $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="6f947-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="6f947-110">Det andra kommandot ändrar egenskapen som har ID-Property11.</span><span class="sxs-lookup"><span data-stu-id="6f947-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="6f947-111">Kommandot tilldelar strängarna i $Tags som taggar på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="6f947-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="6f947-112">Exempel 2: ändra en egenskap så att den har ett hemligt värde</span><span class="sxs-lookup"><span data-stu-id="6f947-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="6f947-113">Det här kommandot ändrar egenskapen som är krypterad.</span><span class="sxs-lookup"><span data-stu-id="6f947-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="6f947-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f947-114">PARAMETERS</span></span>

### <span data-ttu-id="6f947-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6f947-115">-Context</span></span>
<span data-ttu-id="6f947-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6f947-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6f947-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f947-117">-DefaultProfile</span></span>
<span data-ttu-id="6f947-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f947-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f947-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f947-119">-Name</span></span>
<span data-ttu-id="6f947-120">Anger namnet på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="6f947-120">Specifies the name of the property.</span></span>
<span data-ttu-id="6f947-121">Maximal längd är 100 tecken.</span><span class="sxs-lookup"><span data-stu-id="6f947-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="6f947-122">Namn innehåller bara bokstäver, siffror, punkter, streck och under streck.</span><span class="sxs-lookup"><span data-stu-id="6f947-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="6f947-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f947-123">-PassThru</span></span>
<span data-ttu-id="6f947-124">Anger att denna cmdlet returnerar **PsApiManagementProperty** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="6f947-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6f947-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="6f947-125">-PropertyId</span></span>
<span data-ttu-id="6f947-126">Anger ett ID för den egenskap som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="6f947-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6f947-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="6f947-127">-Secret</span></span>
<span data-ttu-id="6f947-128">Anger att egenskap svärdet är en hemlighet och att det är krypterat.</span><span class="sxs-lookup"><span data-stu-id="6f947-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f947-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6f947-129">-Tag</span></span>
<span data-ttu-id="6f947-130">Taggar som är associerade med en egenskap.</span><span class="sxs-lookup"><span data-stu-id="6f947-130">Tags associated with a property.</span></span> <span data-ttu-id="6f947-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="6f947-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f947-132">-Värde</span><span class="sxs-lookup"><span data-stu-id="6f947-132">-Value</span></span>
<span data-ttu-id="6f947-133">Anger ett värde för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="6f947-133">Specifies a value for the property.</span></span>
<span data-ttu-id="6f947-134">Det här värdet kan innehålla princip uttryck.</span><span class="sxs-lookup"><span data-stu-id="6f947-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="6f947-135">Maximal längd är 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="6f947-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="6f947-136">Värdet får inte vara tomt eller bestå av endast blank steg.</span><span class="sxs-lookup"><span data-stu-id="6f947-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="6f947-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f947-137">-Confirm</span></span>
<span data-ttu-id="6f947-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f947-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f947-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f947-139">-WhatIf</span></span>
<span data-ttu-id="6f947-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f947-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f947-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f947-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f947-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f947-142">CommonParameters</span></span>
<span data-ttu-id="6f947-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f947-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f947-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f947-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f947-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f947-145">INPUTS</span></span>

### <span data-ttu-id="6f947-146">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6f947-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f947-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6f947-147">System.String</span></span>

### <span data-ttu-id="6f947-148">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6f947-148">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6f947-149">System. string []</span><span class="sxs-lookup"><span data-stu-id="6f947-149">System.String[]</span></span>

### <span data-ttu-id="6f947-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6f947-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6f947-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f947-151">OUTPUTS</span></span>

### <span data-ttu-id="6f947-152">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6f947-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="6f947-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f947-153">NOTES</span></span>

## <span data-ttu-id="6f947-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f947-154">RELATED LINKS</span></span>

[<span data-ttu-id="6f947-155">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6f947-155">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="6f947-156">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6f947-156">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="6f947-157">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="6f947-157">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


