---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 5273161b18f49e2cfd8f772987d8f0d9ce90bc69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573750"
---
# <span data-ttu-id="4f051-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4f051-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="4f051-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f051-102">SYNOPSIS</span></span>
<span data-ttu-id="4f051-103">Ändrar en API-egenskap.</span><span class="sxs-lookup"><span data-stu-id="4f051-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f051-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f051-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tags <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f051-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f051-105">DESCRIPTION</span></span>
<span data-ttu-id="4f051-106">Cmdleten **set-AzureRmApiManagementProperty** ändrar en egenskap för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="4f051-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="4f051-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f051-107">EXAMPLES</span></span>

### <span data-ttu-id="4f051-108">Exempel 1: ändra taggarna för en egenskap</span><span class="sxs-lookup"><span data-stu-id="4f051-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="4f051-109">Det första kommandot tilldelar två värden till $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="4f051-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="4f051-110">Det andra kommandot ändrar egenskapen som har ID-Property11.</span><span class="sxs-lookup"><span data-stu-id="4f051-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="4f051-111">Kommandot tilldelar strängarna i $Tags som taggar på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="4f051-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="4f051-112">Exempel 2: ändra en egenskap så att den har ett hemligt värde</span><span class="sxs-lookup"><span data-stu-id="4f051-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>Set-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="4f051-113">Det här kommandot ändrar egenskapen som är krypterad.</span><span class="sxs-lookup"><span data-stu-id="4f051-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="4f051-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f051-114">PARAMETERS</span></span>

### <span data-ttu-id="4f051-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4f051-115">-Context</span></span>
<span data-ttu-id="4f051-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4f051-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4f051-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f051-117">-Name</span></span>
<span data-ttu-id="4f051-118">Anger namnet på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="4f051-118">Specifies the name of the property.</span></span>
<span data-ttu-id="4f051-119">Maximal längd är 100 tecken.</span><span class="sxs-lookup"><span data-stu-id="4f051-119">Maximum length is 100 characters.</span></span>
<span data-ttu-id="4f051-120">Namn innehåller bara bokstäver, siffror, punkter, streck och under streck.</span><span class="sxs-lookup"><span data-stu-id="4f051-120">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="4f051-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f051-121">-PassThru</span></span>
<span data-ttu-id="4f051-122">Anger att denna cmdlet returnerar **PsApiManagementProperty** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4f051-122">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4f051-123">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="4f051-123">-PropertyId</span></span>
<span data-ttu-id="4f051-124">Anger ett ID för den egenskap som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4f051-124">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4f051-125">-Secret</span><span class="sxs-lookup"><span data-stu-id="4f051-125">-Secret</span></span>
<span data-ttu-id="4f051-126">Anger att egenskap svärdet är en hemlighet och att det är krypterat.</span><span class="sxs-lookup"><span data-stu-id="4f051-126">Indicates that the property value is a secret and should be encrypted.</span></span>

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

### <span data-ttu-id="4f051-127">-Taggar</span><span class="sxs-lookup"><span data-stu-id="4f051-127">-Tags</span></span>
<span data-ttu-id="4f051-128">Anger en matris med koder som denna cmdlet associerar till egenskapen.</span><span class="sxs-lookup"><span data-stu-id="4f051-128">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="4f051-129">Du kan använda taggar för att filtrera egenskaps listan.</span><span class="sxs-lookup"><span data-stu-id="4f051-129">You can use tags to filter the property list.</span></span>

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

### <span data-ttu-id="4f051-130">-Värde</span><span class="sxs-lookup"><span data-stu-id="4f051-130">-Value</span></span>
<span data-ttu-id="4f051-131">Anger ett värde för egenskapen.</span><span class="sxs-lookup"><span data-stu-id="4f051-131">Specifies a value for the property.</span></span>
<span data-ttu-id="4f051-132">Det här värdet kan innehålla princip uttryck.</span><span class="sxs-lookup"><span data-stu-id="4f051-132">This value can contain policy expressions.</span></span>
<span data-ttu-id="4f051-133">Maximal längd är 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="4f051-133">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="4f051-134">Värdet får inte vara tomt eller bestå av endast blank steg.</span><span class="sxs-lookup"><span data-stu-id="4f051-134">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="4f051-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f051-135">-DefaultProfile</span></span>
<span data-ttu-id="4f051-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f051-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f051-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f051-137">CommonParameters</span></span>
<span data-ttu-id="4f051-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f051-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f051-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f051-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f051-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f051-140">INPUTS</span></span>

## <span data-ttu-id="4f051-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f051-141">OUTPUTS</span></span>

### <span data-ttu-id="4f051-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4f051-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="4f051-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f051-143">NOTES</span></span>

## <span data-ttu-id="4f051-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f051-144">RELATED LINKS</span></span>

[<span data-ttu-id="4f051-145">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4f051-145">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="4f051-146">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4f051-146">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="4f051-147">Remove-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="4f051-147">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


