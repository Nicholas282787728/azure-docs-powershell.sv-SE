---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 76de3ad08e6acb0035cfa2a9ca5d353fcbf38033
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757502"
---
# <span data-ttu-id="aae7b-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="aae7b-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="aae7b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aae7b-102">SYNOPSIS</span></span>
<span data-ttu-id="aae7b-103">Tar bort en DSC-nod från hanteringen av ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="aae7b-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aae7b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aae7b-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aae7b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aae7b-105">DESCRIPTION</span></span>
<span data-ttu-id="aae7b-106">Med cmdleten **Unregistered-AzureRmAutomationDscNode** tar du bort en APS-nod för önskad tillstånds konfiguration (DSC) från hantering av ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="aae7b-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="aae7b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aae7b-107">EXAMPLES</span></span>

### <span data-ttu-id="aae7b-108">Exempel 1: ta bort en Azure DSC-nod från hantering med ett Automation-konto</span><span class="sxs-lookup"><span data-stu-id="aae7b-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="aae7b-109">Det här kommandot tar bort DSC-noden med angivet GUID från hanteringen av Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="aae7b-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="aae7b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aae7b-110">PARAMETERS</span></span>

### <span data-ttu-id="aae7b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aae7b-111">-AutomationAccountName</span></span>
<span data-ttu-id="aae7b-112">Anger namnet på det Automation-konto som den här cmdleten tar bort en DSC-nod från.</span><span class="sxs-lookup"><span data-stu-id="aae7b-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae7b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="aae7b-113">-Force</span></span>
<span data-ttu-id="aae7b-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="aae7b-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae7b-115">-ID</span><span class="sxs-lookup"><span data-stu-id="aae7b-115">-Id</span></span>
<span data-ttu-id="aae7b-116">Anger unikt ID för DSC-noden som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="aae7b-116">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="aae7b-118">Anger namnet på en resurs grupp där denna cmdlet avregistrerar en DSC-nod.</span><span class="sxs-lookup"><span data-stu-id="aae7b-118">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae7b-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aae7b-119">-Confirm</span></span>
<span data-ttu-id="aae7b-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aae7b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae7b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aae7b-121">-WhatIf</span></span>
<span data-ttu-id="aae7b-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aae7b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aae7b-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aae7b-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae7b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae7b-124">-DefaultProfile</span></span>
<span data-ttu-id="aae7b-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aae7b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aae7b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae7b-126">CommonParameters</span></span>
<span data-ttu-id="aae7b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aae7b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae7b-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae7b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae7b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aae7b-129">INPUTS</span></span>

## <span data-ttu-id="aae7b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aae7b-130">OUTPUTS</span></span>

### <span data-ttu-id="aae7b-131">Microsoft. Azure. commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="aae7b-131">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="aae7b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aae7b-132">NOTES</span></span>

## <span data-ttu-id="aae7b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aae7b-133">RELATED LINKS</span></span>

[<span data-ttu-id="aae7b-134">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="aae7b-134">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="aae7b-135">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="aae7b-135">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="aae7b-136">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="aae7b-136">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


