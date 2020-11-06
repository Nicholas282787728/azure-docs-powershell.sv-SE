---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 83f697733d56ae7d99bc0b2660b5abbaca15a71f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585071"
---
# <span data-ttu-id="9bbbe-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9bbbe-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="9bbbe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9bbbe-102">SYNOPSIS</span></span>
<span data-ttu-id="9bbbe-103">Tar bort ett SQL Server-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bbbe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9bbbe-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bbbe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9bbbe-105">DESCRIPTION</span></span>
<span data-ttu-id="9bbbe-106">Cmdleten **Remove-AzureRmVMSqlServerExtension** tar bort ett AzureSQL-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="9bbbe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9bbbe-107">EXAMPLES</span></span>

### <span data-ttu-id="9bbbe-108">Exempel 1: ta bort ett SQL Server-tillägg</span><span class="sxs-lookup"><span data-stu-id="9bbbe-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="9bbbe-109">Det här kommandot tar bort ett SQL Server-tillägg från den virtuella datorn med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="9bbbe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9bbbe-110">PARAMETERS</span></span>

### <span data-ttu-id="9bbbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bbbe-111">-DefaultProfile</span></span>
<span data-ttu-id="9bbbe-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bbbe-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9bbbe-113">-Name</span></span>
<span data-ttu-id="9bbbe-114">Anger namnet på SQL Server tillägget som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bbbe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bbbe-115">-ResourceGroupName</span></span>
<span data-ttu-id="9bbbe-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9bbbe-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="9bbbe-117">-VMName</span></span>
<span data-ttu-id="9bbbe-118">Anger namnet på den virtuella dator från vilken denna cmdlet tar bort SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bbbe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bbbe-119">CommonParameters</span></span>
<span data-ttu-id="9bbbe-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bbbe-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bbbe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bbbe-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9bbbe-122">INPUTS</span></span>

### <span data-ttu-id="9bbbe-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9bbbe-123">System.String</span></span>

## <span data-ttu-id="9bbbe-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9bbbe-124">OUTPUTS</span></span>

### <span data-ttu-id="9bbbe-125">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9bbbe-125">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9bbbe-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9bbbe-126">NOTES</span></span>

## <span data-ttu-id="9bbbe-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9bbbe-127">RELATED LINKS</span></span>

[<span data-ttu-id="9bbbe-128">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9bbbe-128">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="9bbbe-129">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9bbbe-129">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


