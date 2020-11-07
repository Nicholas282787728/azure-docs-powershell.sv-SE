---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 6e3803b7627e16a96c8101f3a6dd1eee5a1b2689
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924938"
---
# <span data-ttu-id="61100-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="61100-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="61100-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61100-102">SYNOPSIS</span></span>
<span data-ttu-id="61100-103">Tar bort ett SQL Server-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="61100-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="61100-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61100-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61100-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61100-105">DESCRIPTION</span></span>
<span data-ttu-id="61100-106">Cmdleten **Remove-AzVMSqlServerExtension** tar bort ett AzureSQL-tillägg från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="61100-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="61100-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61100-107">EXAMPLES</span></span>

### <span data-ttu-id="61100-108">Exempel 1: ta bort ett SQL Server-tillägg</span><span class="sxs-lookup"><span data-stu-id="61100-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="61100-109">Det här kommandot tar bort ett SQL Server-tillägg från den virtuella datorn med namnet ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="61100-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="61100-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61100-110">PARAMETERS</span></span>

### <span data-ttu-id="61100-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61100-111">-DefaultProfile</span></span>
<span data-ttu-id="61100-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61100-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61100-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="61100-113">-Name</span></span>
<span data-ttu-id="61100-114">Anger namnet på SQL Server tillägget som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="61100-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="61100-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61100-115">-ResourceGroupName</span></span>
<span data-ttu-id="61100-116">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="61100-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="61100-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="61100-117">-VMName</span></span>
<span data-ttu-id="61100-118">Anger namnet på den virtuella dator från vilken denna cmdlet tar bort SQL Server-tillägget.</span><span class="sxs-lookup"><span data-stu-id="61100-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="61100-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61100-119">CommonParameters</span></span>
<span data-ttu-id="61100-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61100-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61100-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61100-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61100-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61100-122">INPUTS</span></span>

### <span data-ttu-id="61100-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="61100-123">None</span></span>
<span data-ttu-id="61100-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="61100-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61100-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61100-125">OUTPUTS</span></span>

### <span data-ttu-id="61100-126">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="61100-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="61100-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61100-127">NOTES</span></span>

## <span data-ttu-id="61100-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61100-128">RELATED LINKS</span></span>

[<span data-ttu-id="61100-129">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="61100-129">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="61100-130">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="61100-130">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


