---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525094"
---
# <span data-ttu-id="134cf-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="134cf-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="134cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="134cf-102">SYNOPSIS</span></span>
<span data-ttu-id="134cf-103">Hämtar en lista eller ett visst namngivet värde.</span><span class="sxs-lookup"><span data-stu-id="134cf-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="134cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="134cf-104">SYNTAX</span></span>

### <span data-ttu-id="134cf-105">GetAllNamedValues (standard)</span><span class="sxs-lookup"><span data-stu-id="134cf-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="134cf-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="134cf-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="134cf-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="134cf-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="134cf-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="134cf-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="134cf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="134cf-109">DESCRIPTION</span></span>
<span data-ttu-id="134cf-110">Cmdleten **Get-AzApiManagementNamedValue** hämtar en lista eller ett visst namngivet värde.</span><span class="sxs-lookup"><span data-stu-id="134cf-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="134cf-111">Värdet tas inte med i resultatet om det namngivna värdet är markerat som hemligt.</span><span class="sxs-lookup"><span data-stu-id="134cf-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="134cf-112">Använd **Get-AzApiManagementNamedValueSecretValue** för att få hemligt värde.</span><span class="sxs-lookup"><span data-stu-id="134cf-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="134cf-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="134cf-113">EXAMPLES</span></span>

### <span data-ttu-id="134cf-114">Exempel 1: Hämta namngivet värde efter namn</span><span class="sxs-lookup"><span data-stu-id="134cf-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="134cf-115">Med det här kommandot hämtas den namngivna värde informationen till det namngivna värde namnet.</span><span class="sxs-lookup"><span data-stu-id="134cf-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="134cf-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="134cf-116">PARAMETERS</span></span>

### <span data-ttu-id="134cf-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="134cf-117">-Context</span></span>
<span data-ttu-id="134cf-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="134cf-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="134cf-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="134cf-119">This parameter is required.</span></span>

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

### <span data-ttu-id="134cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134cf-120">-DefaultProfile</span></span>
<span data-ttu-id="134cf-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="134cf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="134cf-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="134cf-122">-Name</span></span>
<span data-ttu-id="134cf-123">Söker efter namngivna värden med namn som innehåller sträng namnet.</span><span class="sxs-lookup"><span data-stu-id="134cf-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="134cf-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="134cf-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="134cf-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="134cf-125">-NamedValueId</span></span>
<span data-ttu-id="134cf-126">ID för det namngivna värdet.</span><span class="sxs-lookup"><span data-stu-id="134cf-126">Identifier of the named value.</span></span>
<span data-ttu-id="134cf-127">Om det anges försöker hitta ett namngivet värde efter ID: till.</span><span class="sxs-lookup"><span data-stu-id="134cf-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="134cf-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="134cf-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="134cf-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="134cf-129">-Tag</span></span>
<span data-ttu-id="134cf-130">Hittar namngivna värden som är associerade med en tagg.</span><span class="sxs-lookup"><span data-stu-id="134cf-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="134cf-131">Om det anges returnerar alla egenskaper kopplade till en tagg.</span><span class="sxs-lookup"><span data-stu-id="134cf-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="134cf-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="134cf-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="134cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134cf-133">CommonParameters</span></span>
<span data-ttu-id="134cf-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="134cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134cf-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="134cf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134cf-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="134cf-136">INPUTS</span></span>

### <span data-ttu-id="134cf-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="134cf-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="134cf-138">System. String</span><span class="sxs-lookup"><span data-stu-id="134cf-138">System.String</span></span>

## <span data-ttu-id="134cf-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="134cf-139">OUTPUTS</span></span>

### <span data-ttu-id="134cf-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="134cf-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="134cf-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="134cf-141">NOTES</span></span>

## <span data-ttu-id="134cf-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="134cf-142">RELATED LINKS</span></span>
