---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProperty.md
ms.openlocfilehash: bed6126dbd1ea57a29d041daf10a3deb05f2dc92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089947"
---
# <span data-ttu-id="968b1-101">New-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="968b1-101">New-AzApiManagementProperty</span></span>

## <span data-ttu-id="968b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="968b1-102">SYNOPSIS</span></span>
<span data-ttu-id="968b1-103">Skapar en ny egenskap.</span><span class="sxs-lookup"><span data-stu-id="968b1-103">Creates a new Property.</span></span>

## <span data-ttu-id="968b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="968b1-104">SYNTAX</span></span>

```
New-AzApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="968b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="968b1-105">DESCRIPTION</span></span>
<span data-ttu-id="968b1-106">Cmdleten **New-AzApiManagementProperty** skapar en Azure API Management- **egenskap**.</span><span class="sxs-lookup"><span data-stu-id="968b1-106">The **New-AzApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="968b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="968b1-107">EXAMPLES</span></span>

### <span data-ttu-id="968b1-108">Exempel 1: skapa en egenskap som innehåller Taggar</span><span class="sxs-lookup"><span data-stu-id="968b1-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="968b1-109">Det första kommandot tilldelar två värden till $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="968b1-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="968b1-110">Det andra kommandot skapar en egenskap och tilldelar strängarna i $Tags som taggar på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="968b1-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="968b1-111">Exempel 2: skapa en egenskap som har ett hemligt värde</span><span class="sxs-lookup"><span data-stu-id="968b1-111">Example 2: Create a property that has a secret value</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property" -Value "Secret Property Value" -Secret
```

<span data-ttu-id="968b1-112">Det här kommandot skapar en **egenskap** som har ett krypterat värde.</span><span class="sxs-lookup"><span data-stu-id="968b1-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="968b1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="968b1-113">PARAMETERS</span></span>

### <span data-ttu-id="968b1-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="968b1-114">-Context</span></span>
<span data-ttu-id="968b1-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="968b1-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="968b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="968b1-116">-DefaultProfile</span></span>
<span data-ttu-id="968b1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="968b1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="968b1-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="968b1-118">-Name</span></span>
<span data-ttu-id="968b1-119">Anger namnet på den egenskap som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="968b1-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="968b1-120">Maximal längd är 100 tecken.</span><span class="sxs-lookup"><span data-stu-id="968b1-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="968b1-121">Namn innehåller bara bokstäver, siffror, punkter, streck och under streck.</span><span class="sxs-lookup"><span data-stu-id="968b1-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="968b1-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="968b1-122">-PropertyId</span></span>
<span data-ttu-id="968b1-123">Anger ett ID för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="968b1-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="968b1-124">Maximal längd är 256 tecken.</span><span class="sxs-lookup"><span data-stu-id="968b1-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="968b1-125">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="968b1-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="968b1-126">-Secret</span><span class="sxs-lookup"><span data-stu-id="968b1-126">-Secret</span></span>
<span data-ttu-id="968b1-127">Anger att egenskap svärdet är en hemlighet och att det är krypterat.</span><span class="sxs-lookup"><span data-stu-id="968b1-127">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="968b1-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="968b1-128">-Tag</span></span>
<span data-ttu-id="968b1-129">Taggar som ska kopplas till egenskapen.</span><span class="sxs-lookup"><span data-stu-id="968b1-129">Tags to be associated with Property.</span></span> <span data-ttu-id="968b1-130">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="968b1-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="968b1-131">-Värde</span><span class="sxs-lookup"><span data-stu-id="968b1-131">-Value</span></span>
<span data-ttu-id="968b1-132">Anger ett värde för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="968b1-132">Specifies a value for the property.</span></span>
<span data-ttu-id="968b1-133">Det här värdet kan innehålla princip uttryck.</span><span class="sxs-lookup"><span data-stu-id="968b1-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="968b1-134">Maximal längd är 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="968b1-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="968b1-135">Värdet får inte vara tomt eller bestå av endast blank steg.</span><span class="sxs-lookup"><span data-stu-id="968b1-135">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="968b1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="968b1-136">CommonParameters</span></span>
<span data-ttu-id="968b1-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="968b1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="968b1-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="968b1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="968b1-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="968b1-139">INPUTS</span></span>

### <span data-ttu-id="968b1-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="968b1-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="968b1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="968b1-141">System.String</span></span>

### <span data-ttu-id="968b1-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="968b1-142">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="968b1-143">System. string []</span><span class="sxs-lookup"><span data-stu-id="968b1-143">System.String[]</span></span>

## <span data-ttu-id="968b1-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="968b1-144">OUTPUTS</span></span>

### <span data-ttu-id="968b1-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="968b1-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="968b1-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="968b1-146">NOTES</span></span>

## <span data-ttu-id="968b1-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="968b1-147">RELATED LINKS</span></span>

[<span data-ttu-id="968b1-148">Remove-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="968b1-148">Remove-AzApiManagementProperty</span></span>](./Remove-AzApiManagementProperty.md)

[<span data-ttu-id="968b1-149">Set-AzApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="968b1-149">Set-AzApiManagementProperty</span></span>](./Set-AzApiManagementProperty.md)


