---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServer.md
ms.openlocfilehash: 76b4e024f5a6d5979bbcd9aa860caee823ecc28e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576399"
---
# <span data-ttu-id="683ed-101">Remove-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="683ed-101">Remove-AzureRmSqlServer</span></span>

## <span data-ttu-id="683ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="683ed-102">SYNOPSIS</span></span>
<span data-ttu-id="683ed-103">Tar bort en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="683ed-103">Removes an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="683ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="683ed-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="683ed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="683ed-105">DESCRIPTION</span></span>
<span data-ttu-id="683ed-106">Cmdleten **Remove-AzureRmSqlServer** tar bort en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="683ed-106">The **Remove-AzureRmSqlServer** cmdlet removes an Azure SQL Database server.</span></span>

<span data-ttu-id="683ed-107">Borttagnings åtgärden är asynkron och kan ta lite tid, så kontrol lera att åtgärden är klar innan du utför ytterligare åtgärder som beror på att servern tas bort helt.</span><span class="sxs-lookup"><span data-stu-id="683ed-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="683ed-108">Till exempel måste du skapa en ny server med samma namn.</span><span class="sxs-lookup"><span data-stu-id="683ed-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="683ed-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="683ed-109">EXAMPLES</span></span>

### <span data-ttu-id="683ed-110">Exempel 1: ta bort en server</span><span class="sxs-lookup"><span data-stu-id="683ed-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="683ed-111">Det här kommandot tar bort Azure SQL-databasfilen med namnet Server01.</span><span class="sxs-lookup"><span data-stu-id="683ed-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="683ed-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="683ed-112">PARAMETERS</span></span>

### <span data-ttu-id="683ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683ed-113">-DefaultProfile</span></span>
<span data-ttu-id="683ed-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="683ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="683ed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="683ed-115">-Force</span></span>
<span data-ttu-id="683ed-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="683ed-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="683ed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="683ed-117">-ResourceGroupName</span></span>
<span data-ttu-id="683ed-118">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="683ed-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="683ed-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="683ed-119">-ServerName</span></span>
<span data-ttu-id="683ed-120">Anger namnet på den server som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="683ed-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="683ed-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="683ed-121">-Confirm</span></span>
<span data-ttu-id="683ed-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="683ed-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="683ed-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="683ed-123">-WhatIf</span></span>
<span data-ttu-id="683ed-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="683ed-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="683ed-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="683ed-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="683ed-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683ed-126">CommonParameters</span></span>
<span data-ttu-id="683ed-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="683ed-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683ed-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="683ed-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683ed-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="683ed-129">INPUTS</span></span>

### <span data-ttu-id="683ed-130">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="683ed-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="683ed-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="683ed-131">OUTPUTS</span></span>

### <span data-ttu-id="683ed-132">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="683ed-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="683ed-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="683ed-133">NOTES</span></span>

## <span data-ttu-id="683ed-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="683ed-134">RELATED LINKS</span></span>

[<span data-ttu-id="683ed-135">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="683ed-135">Get-AzureRmSqlServer</span></span>](./Get-AzureRmSqlServer.md)

[<span data-ttu-id="683ed-136">New-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="683ed-136">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="683ed-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="683ed-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="683ed-138">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="683ed-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


