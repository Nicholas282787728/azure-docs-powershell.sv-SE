---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProperty.md
ms.openlocfilehash: b12a904be944b4a6338ad0bf34a4c906382cb910
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917670"
---
# <span data-ttu-id="4b8fd-101">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4b8fd-101">Set-AzApiManagementProperty</span></span>

## <span data-ttu-id="4b8fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b8fd-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8fd-103">Ändrar en API-egenskap.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-103">Modifies an API Management Property.</span></span>

## <span data-ttu-id="4b8fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b8fd-104">SYNTAX</span></span>

```
Set-AzApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b8fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b8fd-105">DESCRIPTION</span></span>
<span data-ttu-id="4b8fd-106">Cmdleten **set-AzApiManagementProperty** ändrar en egenskap för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-106">The **Set-AzApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="4b8fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b8fd-107">EXAMPLES</span></span>

### <span data-ttu-id="4b8fd-108">Exempel 1: ändra taggarna för en egenskap</span><span class="sxs-lookup"><span data-stu-id="4b8fd-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="4b8fd-109">Det första kommandot tilldelar två värden till $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="4b8fd-110">Det andra kommandot ändrar egenskapen som har ID-Property11.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="4b8fd-111">Kommandot tilldelar strängarna i $Tags som taggar på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="4b8fd-112">Exempel 2: ändra en egenskap så att den har ett hemligt värde</span><span class="sxs-lookup"><span data-stu-id="4b8fd-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="4b8fd-113">Det här kommandot ändrar egenskapen som är krypterad.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="4b8fd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b8fd-114">PARAMETERS</span></span>

### <span data-ttu-id="4b8fd-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4b8fd-115">-Context</span></span>
<span data-ttu-id="4b8fd-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b8fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8fd-117">-DefaultProfile</span></span>
<span data-ttu-id="4b8fd-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b8fd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b8fd-119">-Name</span></span>
<span data-ttu-id="4b8fd-120">Anger namnet på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-120">Specifies the name of the property.</span></span>
<span data-ttu-id="4b8fd-121">Maximal längd är 100 tecken.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="4b8fd-122">Namn innehåller bara bokstäver, siffror, punkter, streck och under streck.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="4b8fd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b8fd-123">-PassThru</span></span>
<span data-ttu-id="4b8fd-124">Anger att denna cmdlet returnerar **PsApiManagementProperty** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4b8fd-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="4b8fd-125">-PropertyId</span></span>
<span data-ttu-id="4b8fd-126">Anger ett ID för den egenskap som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4b8fd-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="4b8fd-127">-Secret</span></span>
<span data-ttu-id="4b8fd-128">Anger att egenskap svärdet är en hemlighet och att det är krypterat.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-128">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="4b8fd-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4b8fd-129">-Tag</span></span>
<span data-ttu-id="4b8fd-130">Taggar som är associerade med en egenskap.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-130">Tags associated with a property.</span></span> <span data-ttu-id="4b8fd-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="4b8fd-132">-Värde</span><span class="sxs-lookup"><span data-stu-id="4b8fd-132">-Value</span></span>
<span data-ttu-id="4b8fd-133">Anger ett värde för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-133">Specifies a value for the property.</span></span>
<span data-ttu-id="4b8fd-134">Det här värdet kan innehålla princip uttryck.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="4b8fd-135">Maximal längd är 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="4b8fd-136">Värdet får inte vara tomt eller bestå av endast blank steg.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="4b8fd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8fd-137">CommonParameters</span></span>
<span data-ttu-id="4b8fd-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b8fd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8fd-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b8fd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8fd-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b8fd-140">INPUTS</span></span>

### <span data-ttu-id="4b8fd-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4b8fd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b8fd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4b8fd-142">System.String</span></span>

### <span data-ttu-id="4b8fd-143">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4b8fd-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4b8fd-144">System. string []</span><span class="sxs-lookup"><span data-stu-id="4b8fd-144">System.String[]</span></span>

### <span data-ttu-id="4b8fd-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4b8fd-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4b8fd-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b8fd-146">OUTPUTS</span></span>

### <span data-ttu-id="4b8fd-147">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4b8fd-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="4b8fd-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b8fd-148">NOTES</span></span>

## <span data-ttu-id="4b8fd-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b8fd-149">RELATED LINKS</span></span>

[<span data-ttu-id="4b8fd-150">Get-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4b8fd-150">Get-AzApiManagementProperty</span></span>](./Get-AzApiManagementProperty.md)

[<span data-ttu-id="4b8fd-151">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4b8fd-151">New-AzApiManagementProperty</span></span>](./New-AzApiManagementProperty.md)

[<span data-ttu-id="4b8fd-152">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4b8fd-152">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)


