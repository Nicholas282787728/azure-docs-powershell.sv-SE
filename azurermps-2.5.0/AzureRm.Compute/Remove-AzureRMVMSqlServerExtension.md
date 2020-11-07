---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: aa37745469ad6610fa2511d49c3404bbf54d8059
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930674"
---
# <span data-ttu-id="2a435-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2a435-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="2a435-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a435-102">SYNOPSIS</span></span>
<span data-ttu-id="2a435-103">Tar bort ett SQL Server-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2a435-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a435-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a435-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a435-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a435-105">DESCRIPTION</span></span>
<span data-ttu-id="2a435-106">Cmdleten **Remove-AzureRmVMSqlServerExtension** tar bort ett AzureSQL-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="2a435-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="2a435-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a435-107">EXAMPLES</span></span>

### <span data-ttu-id="2a435-108">Exempel 1: ta bort ett SQL Server-tillägg</span><span class="sxs-lookup"><span data-stu-id="2a435-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="2a435-109">Det här kommandot tar bort ett SQL Server-tillägg från den virtuella datorn med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="2a435-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="2a435-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a435-110">PARAMETERS</span></span>

### <span data-ttu-id="2a435-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a435-111">-DefaultProfile</span></span>
<span data-ttu-id="2a435-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a435-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a435-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a435-113">-Name</span></span>
<span data-ttu-id="2a435-114">Anger namnet på SQL Server tillägget som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="2a435-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a435-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a435-115">-ResourceGroupName</span></span>
<span data-ttu-id="2a435-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2a435-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2a435-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="2a435-117">-VMName</span></span>
<span data-ttu-id="2a435-118">Anger namnet på den virtuella dator från vilken denna cmdlet tar bort SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="2a435-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a435-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a435-119">CommonParameters</span></span>
<span data-ttu-id="2a435-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a435-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a435-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a435-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a435-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a435-122">INPUTS</span></span>

### <span data-ttu-id="2a435-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="2a435-123">None</span></span>
<span data-ttu-id="2a435-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2a435-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a435-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a435-125">OUTPUTS</span></span>

### <span data-ttu-id="2a435-126">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2a435-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2a435-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a435-127">NOTES</span></span>

## <span data-ttu-id="2a435-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a435-128">RELATED LINKS</span></span>

[<span data-ttu-id="2a435-129">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2a435-129">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="2a435-130">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="2a435-130">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


