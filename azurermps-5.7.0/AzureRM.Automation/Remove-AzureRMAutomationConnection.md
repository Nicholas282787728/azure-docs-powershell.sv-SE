---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 4fb4bbab5c774cacd274754a106aacfeebdb533c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585176"
---
# <span data-ttu-id="0d5a7-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0d5a7-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="0d5a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d5a7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5a7-103">Tar bort en automatiserings anslutning.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d5a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d5a7-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d5a7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d5a7-105">DESCRIPTION</span></span>
<span data-ttu-id="0d5a7-106">Cmdleten **Remove-AzureRmAutomationConnection** tar bort en anslutning från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="0d5a7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d5a7-107">EXAMPLES</span></span>

### <span data-ttu-id="0d5a7-108">Exempel 1: ta bort en anslutning</span><span class="sxs-lookup"><span data-stu-id="0d5a7-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0d5a7-109">Det här kommandot tar bort ett certifikat som heter ContosoConnection i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0d5a7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d5a7-110">PARAMETERS</span></span>

### <span data-ttu-id="0d5a7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0d5a7-111">-AutomationAccountName</span></span>
<span data-ttu-id="0d5a7-112">Anger namnet på det Automation-konto som denna cmdlet tar bort en anslutning för.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5a7-113">-DefaultProfile</span></span>
<span data-ttu-id="0d5a7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0d5a7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d5a7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0d5a7-115">-Force</span></span>
<span data-ttu-id="0d5a7-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0d5a7-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5a7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d5a7-117">-Name</span></span>
<span data-ttu-id="0d5a7-118">Anger namnet på den anslutning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-118">Specifies the name of the connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d5a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d5a7-120">Anger namnet på den resurs grupp för vilken denna cmdlet tar bort en anslutning.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5a7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d5a7-121">-Confirm</span></span>
<span data-ttu-id="0d5a7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d5a7-123">-WhatIf</span></span>
<span data-ttu-id="0d5a7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d5a7-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5a7-126">CommonParameters</span></span>
<span data-ttu-id="0d5a7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5a7-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5a7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d5a7-129">INPUTS</span></span>

### <span data-ttu-id="0d5a7-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="0d5a7-130">None</span></span>
<span data-ttu-id="0d5a7-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0d5a7-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0d5a7-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d5a7-132">OUTPUTS</span></span>

## <span data-ttu-id="0d5a7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d5a7-133">NOTES</span></span>

## <span data-ttu-id="0d5a7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d5a7-134">RELATED LINKS</span></span>

[<span data-ttu-id="0d5a7-135">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0d5a7-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="0d5a7-136">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="0d5a7-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


