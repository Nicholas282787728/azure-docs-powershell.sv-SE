---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: 55ef0d4ef714c1d434915def403f5560244a3697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758361"
---
# <span data-ttu-id="3f550-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3f550-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="3f550-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f550-102">SYNOPSIS</span></span>
<span data-ttu-id="3f550-103">Skapar en ny egenskap.</span><span class="sxs-lookup"><span data-stu-id="3f550-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f550-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f550-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f550-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f550-105">DESCRIPTION</span></span>
<span data-ttu-id="3f550-106">Cmdleten **New-AzureRmApiManagementProperty** skapar en Azure API Management- **egenskap**.</span><span class="sxs-lookup"><span data-stu-id="3f550-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="3f550-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f550-107">EXAMPLES</span></span>

### <span data-ttu-id="3f550-108">Exempel 1: skapa en egenskap som innehåller Taggar</span><span class="sxs-lookup"><span data-stu-id="3f550-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="3f550-109">Det första kommandot tilldelar två värden till $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="3f550-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="3f550-110">Det andra kommandot skapar en egenskap och tilldelar strängarna i $Tags som taggar på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="3f550-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="3f550-111">Exempel 2: skapa en egenskap som har ett hemligt värde</span><span class="sxs-lookup"><span data-stu-id="3f550-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="3f550-112">Det här kommandot skapar en **egenskap** som har ett krypterat värde.</span><span class="sxs-lookup"><span data-stu-id="3f550-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="3f550-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f550-113">PARAMETERS</span></span>

### <span data-ttu-id="3f550-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3f550-114">-Context</span></span>
<span data-ttu-id="3f550-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3f550-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3f550-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f550-116">-DefaultProfile</span></span>
<span data-ttu-id="3f550-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f550-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3f550-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f550-118">-Name</span></span>
<span data-ttu-id="3f550-119">Anger namnet på den egenskap som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="3f550-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="3f550-120">Maximal längd är 100 tecken.</span><span class="sxs-lookup"><span data-stu-id="3f550-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="3f550-121">Namn innehåller bara bokstäver, siffror, punkter, streck och under streck.</span><span class="sxs-lookup"><span data-stu-id="3f550-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="3f550-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="3f550-122">-PropertyId</span></span>
<span data-ttu-id="3f550-123">Anger ett ID för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="3f550-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="3f550-124">Maximal längd är 256 tecken.</span><span class="sxs-lookup"><span data-stu-id="3f550-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="3f550-125">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="3f550-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="3f550-126">-Secret</span><span class="sxs-lookup"><span data-stu-id="3f550-126">-Secret</span></span>
<span data-ttu-id="3f550-127">Anger att egenskap svärdet är en hemlighet och att det är krypterat.</span><span class="sxs-lookup"><span data-stu-id="3f550-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="3f550-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="3f550-128">-Tag</span></span>
<span data-ttu-id="3f550-129">Taggar som ska kopplas till egenskapen.</span><span class="sxs-lookup"><span data-stu-id="3f550-129">Tags to be associated with Property.</span></span> <span data-ttu-id="3f550-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="3f550-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="3f550-131">-Värde</span><span class="sxs-lookup"><span data-stu-id="3f550-131">-Value</span></span>
<span data-ttu-id="3f550-132">Anger ett värde för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="3f550-132">Specifies a value for the property.</span></span>
<span data-ttu-id="3f550-133">Det här värdet kan innehålla princip uttryck.</span><span class="sxs-lookup"><span data-stu-id="3f550-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="3f550-134">Maximal längd är 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="3f550-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="3f550-135">Värdet får inte vara tomt eller bestå av endast blank steg.</span><span class="sxs-lookup"><span data-stu-id="3f550-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="3f550-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f550-136">CommonParameters</span></span>
<span data-ttu-id="3f550-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f550-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f550-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f550-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f550-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f550-139">INPUTS</span></span>

### <span data-ttu-id="3f550-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="3f550-140">None</span></span>
<span data-ttu-id="3f550-141">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3f550-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f550-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f550-142">OUTPUTS</span></span>

### <span data-ttu-id="3f550-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3f550-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="3f550-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f550-144">NOTES</span></span>

## <span data-ttu-id="3f550-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f550-145">RELATED LINKS</span></span>

[<span data-ttu-id="3f550-146">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3f550-146">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="3f550-147">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3f550-147">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


