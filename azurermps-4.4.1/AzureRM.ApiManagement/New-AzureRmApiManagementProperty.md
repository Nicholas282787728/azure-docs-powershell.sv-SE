---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757515"
---
# <span data-ttu-id="876ec-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="876ec-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="876ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="876ec-102">SYNOPSIS</span></span>
<span data-ttu-id="876ec-103">Skapar en ny egenskap.</span><span class="sxs-lookup"><span data-stu-id="876ec-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="876ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="876ec-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="876ec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="876ec-105">DESCRIPTION</span></span>
<span data-ttu-id="876ec-106">Cmdleten **New-AzureRmApiManagementProperty** skapar en Azure API Management- **egenskap**.</span><span class="sxs-lookup"><span data-stu-id="876ec-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="876ec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="876ec-107">EXAMPLES</span></span>

### <span data-ttu-id="876ec-108">Exempel 1: skapa en egenskap som innehåller Taggar</span><span class="sxs-lookup"><span data-stu-id="876ec-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="876ec-109">Det första kommandot tilldelar två värden till $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="876ec-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="876ec-110">Det andra kommandot skapar en egenskap och tilldelar strängarna i $Tags som taggar på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="876ec-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="876ec-111">Exempel 2: skapa en egenskap som har ett hemligt värde</span><span class="sxs-lookup"><span data-stu-id="876ec-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="876ec-112">Det här kommandot skapar en **egenskap** som har ett krypterat värde.</span><span class="sxs-lookup"><span data-stu-id="876ec-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="876ec-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="876ec-113">PARAMETERS</span></span>

### <span data-ttu-id="876ec-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="876ec-114">-Context</span></span>
<span data-ttu-id="876ec-115">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="876ec-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="876ec-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="876ec-116">-Name</span></span>
<span data-ttu-id="876ec-117">Anger namnet på den egenskap som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="876ec-117">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="876ec-118">Maximal längd är 100 tecken.</span><span class="sxs-lookup"><span data-stu-id="876ec-118">Maximum length is 100 characters.</span></span>
<span data-ttu-id="876ec-119">Namn innehåller bara bokstäver, siffror, punkter, streck och under streck.</span><span class="sxs-lookup"><span data-stu-id="876ec-119">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="876ec-120">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="876ec-120">-PropertyId</span></span>
<span data-ttu-id="876ec-121">Anger ett ID för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="876ec-121">Specifies an ID for the property.</span></span>
<span data-ttu-id="876ec-122">Maximal längd är 256 tecken.</span><span class="sxs-lookup"><span data-stu-id="876ec-122">Maximum length is 256 characters.</span></span>
<span data-ttu-id="876ec-123">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="876ec-123">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="876ec-124">-Secret</span><span class="sxs-lookup"><span data-stu-id="876ec-124">-Secret</span></span>
<span data-ttu-id="876ec-125">Anger att egenskap svärdet är en hemlighet och att det är krypterat.</span><span class="sxs-lookup"><span data-stu-id="876ec-125">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="876ec-126">-Taggar</span><span class="sxs-lookup"><span data-stu-id="876ec-126">-Tags</span></span>
<span data-ttu-id="876ec-127">Anger en matris med koder som denna cmdlet associerar till egenskapen.</span><span class="sxs-lookup"><span data-stu-id="876ec-127">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="876ec-128">Du kan använda taggar för att filtrera egenskaps listan.</span><span class="sxs-lookup"><span data-stu-id="876ec-128">You can use tags to filter the property list.</span></span>

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

### <span data-ttu-id="876ec-129">-Värde</span><span class="sxs-lookup"><span data-stu-id="876ec-129">-Value</span></span>
<span data-ttu-id="876ec-130">Anger ett värde för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="876ec-130">Specifies a value for the property.</span></span>
<span data-ttu-id="876ec-131">Det här värdet kan innehålla princip uttryck.</span><span class="sxs-lookup"><span data-stu-id="876ec-131">This value can contain policy expressions.</span></span>
<span data-ttu-id="876ec-132">Maximal längd är 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="876ec-132">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="876ec-133">Värdet får inte vara tomt eller bestå av endast blank steg.</span><span class="sxs-lookup"><span data-stu-id="876ec-133">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="876ec-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876ec-134">-DefaultProfile</span></span>
<span data-ttu-id="876ec-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="876ec-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="876ec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876ec-136">CommonParameters</span></span>
<span data-ttu-id="876ec-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="876ec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876ec-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="876ec-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876ec-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="876ec-139">INPUTS</span></span>

## <span data-ttu-id="876ec-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="876ec-140">OUTPUTS</span></span>

### <span data-ttu-id="876ec-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="876ec-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="876ec-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="876ec-142">NOTES</span></span>

## <span data-ttu-id="876ec-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="876ec-143">RELATED LINKS</span></span>

[<span data-ttu-id="876ec-144">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="876ec-144">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="876ec-145">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="876ec-145">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


