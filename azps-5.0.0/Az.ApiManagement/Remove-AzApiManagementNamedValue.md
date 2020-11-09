---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326045"
---
# <span data-ttu-id="d4696-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="d4696-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="d4696-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4696-102">SYNOPSIS</span></span>
<span data-ttu-id="d4696-103">Tar bort ett API-Management-namngivet värde.</span><span class="sxs-lookup"><span data-stu-id="d4696-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="d4696-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4696-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4696-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4696-105">DESCRIPTION</span></span>
<span data-ttu-id="d4696-106">Cmdleten **Remove-AzApiManagementNamedValue** tar bort ett Azure API Management **namet-värde**.</span><span class="sxs-lookup"><span data-stu-id="d4696-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="d4696-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4696-107">EXAMPLES</span></span>

### <span data-ttu-id="d4696-108">Exempel 1: ta bort det namngivna värdet</span><span class="sxs-lookup"><span data-stu-id="d4696-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="d4696-109">Det här kommandot tar bort det namngivna värdet med ID-Property11.</span><span class="sxs-lookup"><span data-stu-id="d4696-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="d4696-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4696-110">PARAMETERS</span></span>

### <span data-ttu-id="d4696-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d4696-111">-Context</span></span>
<span data-ttu-id="d4696-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d4696-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d4696-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d4696-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d4696-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4696-114">-DefaultProfile</span></span>
<span data-ttu-id="d4696-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4696-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4696-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="d4696-116">-NamedValueId</span></span>
<span data-ttu-id="d4696-117">Identifierare för befintligt namngivet värde.</span><span class="sxs-lookup"><span data-stu-id="d4696-117">Identifier of existing named value.</span></span>
<span data-ttu-id="d4696-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d4696-118">This parameter is required.</span></span>

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

### <span data-ttu-id="d4696-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4696-119">-PassThru</span></span>
<span data-ttu-id="d4696-120">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="d4696-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d4696-121">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d4696-121">This parameter is optional.</span></span>
<span data-ttu-id="d4696-122">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="d4696-122">Default value is false.</span></span>

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

### <span data-ttu-id="d4696-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4696-123">-Confirm</span></span>
<span data-ttu-id="d4696-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4696-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4696-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4696-125">-WhatIf</span></span>
<span data-ttu-id="d4696-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4696-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4696-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4696-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4696-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4696-128">CommonParameters</span></span>
<span data-ttu-id="d4696-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4696-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4696-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4696-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4696-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4696-131">INPUTS</span></span>

### <span data-ttu-id="d4696-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d4696-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d4696-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d4696-133">System.String</span></span>

### <span data-ttu-id="d4696-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d4696-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d4696-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4696-135">OUTPUTS</span></span>

### <span data-ttu-id="d4696-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4696-136">System.Boolean</span></span>

## <span data-ttu-id="d4696-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4696-137">NOTES</span></span>

## <span data-ttu-id="d4696-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4696-138">RELATED LINKS</span></span>
