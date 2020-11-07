---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 89612136023173d2f725c8c4b286a270400f8c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757423"
---
# <span data-ttu-id="29e87-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="29e87-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="29e87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29e87-102">SYNOPSIS</span></span>
<span data-ttu-id="29e87-103">Ändrar en API-egenskap.</span><span class="sxs-lookup"><span data-stu-id="29e87-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29e87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29e87-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29e87-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29e87-105">DESCRIPTION</span></span>
<span data-ttu-id="29e87-106">Cmdleten **set-AzureRmApiManagementProperty** ändrar en egenskap för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="29e87-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="29e87-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29e87-107">EXAMPLES</span></span>

### <span data-ttu-id="29e87-108">Exempel 1: ändra taggarna för en egenskap</span><span class="sxs-lookup"><span data-stu-id="29e87-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="29e87-109">Det första kommandot tilldelar två värden till $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="29e87-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="29e87-110">Det andra kommandot ändrar egenskapen som har ID-Property11.</span><span class="sxs-lookup"><span data-stu-id="29e87-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="29e87-111">Kommandot tilldelar strängarna i $Tags som taggar på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="29e87-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="29e87-112">Exempel 2: ändra en egenskap så att den har ett hemligt värde</span><span class="sxs-lookup"><span data-stu-id="29e87-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="29e87-113">Det här kommandot ändrar egenskapen som är krypterad.</span><span class="sxs-lookup"><span data-stu-id="29e87-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="29e87-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29e87-114">PARAMETERS</span></span>

### <span data-ttu-id="29e87-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="29e87-115">-Context</span></span>
<span data-ttu-id="29e87-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="29e87-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e87-117">-DefaultProfile</span></span>
<span data-ttu-id="29e87-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29e87-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="29e87-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="29e87-119">-Name</span></span>
<span data-ttu-id="29e87-120">Anger namnet på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="29e87-120">Specifies the name of the property.</span></span>
<span data-ttu-id="29e87-121">Maximal längd är 100 tecken.</span><span class="sxs-lookup"><span data-stu-id="29e87-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="29e87-122">Namn innehåller bara bokstäver, siffror, punkter, streck och under streck.</span><span class="sxs-lookup"><span data-stu-id="29e87-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e87-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29e87-123">-PassThru</span></span>
<span data-ttu-id="29e87-124">Anger att denna cmdlet returnerar **PsApiManagementProperty** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="29e87-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e87-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="29e87-125">-PropertyId</span></span>
<span data-ttu-id="29e87-126">Anger ett ID för den egenskap som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="29e87-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="29e87-127">-Secret</span><span class="sxs-lookup"><span data-stu-id="29e87-127">-Secret</span></span>
<span data-ttu-id="29e87-128">Anger att egenskap svärdet är en hemlighet och att det är krypterat.</span><span class="sxs-lookup"><span data-stu-id="29e87-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e87-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="29e87-129">-Tag</span></span>
<span data-ttu-id="29e87-130">Taggar som är associerade med en egenskap.</span><span class="sxs-lookup"><span data-stu-id="29e87-130">Tags associated with a property.</span></span> <span data-ttu-id="29e87-131">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="29e87-131">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e87-132">-Värde</span><span class="sxs-lookup"><span data-stu-id="29e87-132">-Value</span></span>
<span data-ttu-id="29e87-133">Anger ett värde för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="29e87-133">Specifies a value for the property.</span></span>
<span data-ttu-id="29e87-134">Det här värdet kan innehålla princip uttryck.</span><span class="sxs-lookup"><span data-stu-id="29e87-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="29e87-135">Maximal längd är 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="29e87-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="29e87-136">Värdet får inte vara tomt eller bestå av endast blank steg.</span><span class="sxs-lookup"><span data-stu-id="29e87-136">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29e87-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e87-137">CommonParameters</span></span>
<span data-ttu-id="29e87-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29e87-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e87-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29e87-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e87-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29e87-140">INPUTS</span></span>

### <span data-ttu-id="29e87-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="29e87-141">None</span></span>
<span data-ttu-id="29e87-142">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="29e87-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29e87-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29e87-143">OUTPUTS</span></span>

### <span data-ttu-id="29e87-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="29e87-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="29e87-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29e87-145">NOTES</span></span>

## <span data-ttu-id="29e87-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29e87-146">RELATED LINKS</span></span>

[<span data-ttu-id="29e87-147">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="29e87-147">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="29e87-148">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="29e87-148">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="29e87-149">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="29e87-149">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


